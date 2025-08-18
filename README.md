# DewDew Snippets

<p align="center">
  <img src="https://github.com/yeonjulee1005/dewdew-snippets/blob/d6183ecde9a1cc222b23092f8b1ede32ca3a5964/images/icon.png" width='180px' height='180px' alt="snippet" >
</p>

<p align="center">
  <img src="https://img.shields.io/visual-studio-marketplace/v/dewdew.dewdew-snippets" />
  <h4 align="center">DewDew Snippets for Frontend Developer</h4>
  <br />
</p>

## Overview

A collection of useful code snippets for frontend developers.

- Vue3
- Nuxt4
- React
- React Native
- Next.js

## Installation

Search for "DewDew Snippets" in the marketplace or download the `.vsix` file and install it manually.

## Available Snippets

### Vue3 Snippets

> Create Vue3 Composition API Component

- `ddv3c`

```typescript
<script setup lang="ts">
import { ref, computed, onMounted } from 'vue'

const props = withDefaults(
  defineProps<{
    title?: string
  }>(),
  {
    title: 'Title'
  }
)

const emit = defineEmits([
  'update-title'
])

const count = ref(0)

const doubleCount = computed(() => {
  return count.value * 2
})

const increment = () => {
  count.value++
}

onMounted(() => {
  console.log('Component mounted')
})
</script>

<style scoped lang="scss">
  /* Add your styles here */
</style>

<template>
  <div>
    Hello World
  </div>
</template>
```

> Create Vue3 Pinia Store

- `ddv3p`


```typescript
<script setup lang="ts">
import { defineStore } from 'pinia'
import { ref, computed } from 'vue'

export const useCounterStore = defineStore('counter', () => {
  const count = ref(0)
  const name = ref('Counter')

  const doubleCount = computed(() => {
    return count.value * 2
  })

  const formattedName = computed(() => {
    return `${name.value} Store`
  })

  const increment = () => {
    count.value++
  }

  return {
    count,
    name,
    doubleCount,
    formattedName,
    increment,
  }
})

</script>
```

> Create Vue3 Router Navigation

- `ddv3r`

```typescript
<script setup lang="ts">
import { useRouter, useRoute } from 'vue-router'

const router = useRouter()
const route = useRoute()

const navigateToHome = () => {
  router.push({
    name: 'home',
    params: {
      id: route.params.id
    }
  })
}

const goBack = () => {
  router.back()
}

const goForward = () => {
  router.forward()
}

const goToPath = (path: string) => {
  router.push(path)
}
</script>
```

### Nuxt4 Snippets

> Create Nuxt4 Page

- `ddn4p`

```typescript
<script setup lang="ts">
useHead({
  title: 'Home',
  meta: [
    { name: 'description', content: 'Home Page' }
  ]
})
</script>

<template>
  <div>
    Home Page
  </div>
</template>

<style scoped lang="scss">
  /* Add your styles here */
</style>
```

> Create Nuxt4 Layout

- `ddn4l`

```typescript
<script setup lang="ts">
</script>

<template>
  <div>
    Add your layout Architecture here
  </div>
</template>

<style scoped lang="scss">
  /* Add your styles here */
</style>
```

> Create Nuxt4 Component

- `ddn4c`

```typescript
<script setup lang="ts">
const props = withDefaults(
  defineProps<{
    title?: string
  }>(),
  {
    title: 'Title'
  }
)

const emit = defineEmits([
  'update-title'
])
</script>

<template>
  <div>
    This is Component
  </div>
</template>

<style scoped lang="scss">
  /* Add your styles here */
</style>
```

> Create Nuxt4 Composable

- `ddn4cp`

```typescript
<script setup lang="ts">
export const useCounter = () => {
  const count = useState('count', () => 0)

  const doubleCount = computed(() => {
    return count.value * 2
  })

  const increment = async () => {
    try {
      count.value++
    } catch (error) {
      console.error('Error:', error)
    }
  }

  return {
    count,
    doubleCount,
    increment,
  }
}
```

> Create Nuxt4 Server Route

- `ddn4sr`

```typescript
<script setup lang="ts">
export default defineEventHandler(async (event) => {
  try {
    const query = getQuery(event)
    const param = query.param

    const body = await readBody(event)

    const result = await processData(body)

    return {
      success: true,
      data: result,
      timestamp: new Date().toISOString()
    }
  } catch (error) {
    throw createError({
      statusCode: 500,
      statusMessage: error.message || 'Internal Server Error'
    })
  }
})
```

> Create Nuxt4 Middleware

- `ddn4m`

```typescript
<script setup lang="ts">
export default defineNuxtRouteMiddleware((to, from) => {
  const { user } = useNuxtApp()

  if (!user) {
    return navigateTo('/login')
  }

  /* Add your middleware logic here */
})
</script>
```

> Create Nuxt4 Plugin

- `ddn4pl`

```typescript
<script setup lang="ts">
export default defineNuxtPlugin((nuxtApp) => {
  nuxtApp.provide('global-utility', {
    /* Add your global utility here */
  })
})

nuxtApp.globalProperty = /* Add your global property here */

nuxtApp.hook('app:created', () => {
  /* Add your app lifecycle hook here */
})
</script>
```

### React Snippets

> Create React Functional Component

- `ddrfc`

```tsx
import React from 'react'

interface $Props {
  title?: string
}

const Component = ({ title }: ComponentProps) => {
  return (
    <div>
      {title}
    </div>
  )
}

export default Component
```

> Create React Functional Component with Hooks

- `ddrfch`

```tsx
import React, { useState, useEffect, useCallback, useMemo } from 'react'

interface ComponentProps {
  title?: string
}

const Component = ({ title }: ComponentProps) => {
  const [count, setCount] = useState(0)

  const doubleCount = useMemo(() => {
    return count * 2
  }, [count])

  const increment = useCallback(() => {
    setCount(count + 1)
  }, [count])

  useEffect(() => {
    console.log('Component mounted')

    return () => {
      console.log('Component unmounted')
    }
  }, [])

  return (
    <div>
      {title}
    </div>
  )
}

export default Component
```

> Create React Custom Hook

- `ddrcu`

```tsx
import { useState, useEffect, useCallback } from 'react'

const useComponent = () => {
  const [count, setCount] = useState(0)

  const increment = useCallback(() => {
    setCount(count + 1)
  }, [count])

  useEffect(() => {
    console.log('Component mounted')

    return () => {
      console.log('Component unmounted')
    }
  }, [])

  return {
    count,
    increment,
  }
}

export default useComponent
```

> Create Zustand Local Store

- `ddzls`

```tsx
import { create } from 'zustand'
import { devtools } from 'zustand/middleware'

interface ComponentState {
  count: number,
  isLoading: boolean,
  error: string | null
}

interface ComponentActions {
  increment: () => void
  decrement: () => void
  setLoading: (loading: boolean) => void
  setError: (error: string | null) => void
  reset: () => void
}

const initialState: ComponentState = {
  count: 0,
  isLoading: false,
  error: null
}

export const useComponentStore = create<ComponentState & ComponentActions>()(
  devtools(
    (set, get) => ({
      ...initialState,
      increment: () => {
        set((state) => ({
          count: state.count + 1
        }))
      },
      decrement: () => {
        set((state) => ({
          count: state.count - 1
        }))
      },
      setLoading: (loading) => {
        set({ isLoading: loading })
      },
      setError: (error) => {
        set({ error })
      },
      reset: () => {
        set(initialState)
      }
    }),
    {
      name: 'ComponentStore'
    }
  )
)
```

> Create Zustand Global Store

- `ddzgs`

```tsx
import { create } from 'zustand'
import { devtools, persist } from 'zustand/middleware'
import { subscribeWithSelector } from 'zustand/middleware'

interface ComponentState {
  user: {
    id: string
    name: string
    email: string
    isAuthenticated: boolean
  } | null
  theme: 'light' | 'dark'
  language: 'ko' | 'en'
  notifications: Array<{
    id: string
    message: string
    type: 'info' | 'success' | 'warning' | 'error'
    timestamp: number
  }>
}

interface ComponentActions {
  setUser: (user: ComponentState['user']) => void
  logout: () => void
  toggleTheme: () => void
  setLanguage: (lang: 'ko' | 'en') => void
  addNotification: (notification: Omit<ComponentState['notifications'], 'id' | 'timestamp'>) => void
  removeNotification: (id: string) => void
  clearNotifications: () => void
}

const initialState: ComponentState = {
  user: null,
  theme: 'light',
  language: 'ko',
  notifications: []
}

export const useComponentStore = create<ComponentState & ComponentActions>()(
  devtools(
    persist(
      subscribeWithSelector((set, get) => ({
        ...initialState,
        setUser: (user) => {
          set({ user })
        },
        logout: () => {
          set({ user: null })
        },
        toggleTheme: () => {
          set((state) => ({
            theme: state.theme === 'light' ? 'dark' : 'light'
          }))
        },
        setLanguage: (lang) => {
          set({ language: lang })
        },
        addNotification: (notification) => {
          const newNotification = {
            ...notification,
            id: Date.now().toString(),
            timestamp: Date.now()
          }
          set((state) => ({
            notifications: [...state.notifications, newNotification]
          }))
        },
        removeNotification: (id) => {
          set((state) => ({
            notifications: state.notifications.filter((n) => n.id !== id)
          }))
        },
        clearNotifications: () => {
          set({ notifications: [] })
        }
      })
    ),
    {
      name: 'ComponentStore',
      partialize: (state) => ({
        theme: state.theme,
        language: state.language
      })
    },
    {
      name: 'ComponentStore'
    }
  )
)
```

> Create React Context

- `ddrc`

```tsx
import React, { createContext, useContext, useReducer, ReactNode } from 'react'

interface ContextState {
  count: number,
  isLoading: boolean,
  error: string | null
}

interface ContextAction {
  type: 'INCREMENT' | 'DECREMENT' | 'SET_LOADING' | 'SET_ERROR'
  payload?: any
}

const initialState: ContextState = {
  count: 0,
  isLoading: false,
  error: null
}

const ContextContext = createContext<{
  state: ContextState
  dispatch: React.Dispatch<ContextAction>
} | undefined>(undefined)

const ContextReducer = (state: ContextState, action: ContextAction): ContextState => {
  switch (action.type) {
    case 'INCREMENT':
      return {
        ...state,
        count: state.count + 1
      }
    case 'DECREMENT':
      return {
        ...state,
        count: state.count - 1
      }
    case 'SET_LOADING':
      return {
        ...state,
        isLoading: action.payload
      }
    case 'SET_ERROR':
      return {
        ...state,
        error: action.payload
      }
    default:
      return state
  }
}

export const ContextProvider: React.FC<{ children: ReactNode }> = ({ children }) => {
  const [state, dispatch] = useReducer(ContextReducer, initialState)

  return (
    <ContextContext.Provider value={{ state, dispatch }}>
      {children}
    </ContextContext.Provider>
  )
}

export const useContext = () => {
  const context = useContext(ContextContext)
  if (!context) {
    throw new Error('useContext must be used within a ContextProvider')
  }
  return context
}
```

> Create React Event Handler

- `ddrev`

```tsx
const handle${1:${TM_FILENAME_BASE}InputChange} = (e: React.ChangeEvent<HTMLInputElement>) => {
  const value = e.target.value
  ${2:setValue(value)}
}

const handle${3:${TM_FILENAME_BASE}ButtonClick} = (e: React.MouseEvent<HTMLButtonElement>) => {
  e.preventDefault()
  ${4:handleSubmit()}
}

const handle${5:${TM_FILENAME_BASE}FormSubmit} = (e: React.FormEvent<HTMLFormElement>) => {
  e.preventDefault()
  ${6:submitForm()}
}

const handle${7:${TM_FILENAME_BASE}SelectChange} = (e: React.ChangeEvent<HTMLSelectElement>) => {
  const value = e.target.value
  ${8:setSelectedValue(value)}
}

const handle${9:${TM_FILENAME_BASE}CheckboxChange} = (e: React.ChangeEvent<HTMLInputElement>) => {
  const checked = e.target.checked
  ${10:setIsChecked(checked)}
}
```

### React Native Snippets

> Create React Native Functional Component

- `ddrnfc`

```tsx
import React from 'react'
import { View, StyleSheet } from 'react-native'

interface ComponentProps {
  title?: string
}

const Component = ({ title }: ComponentProps) => {
  return (
    <View style={styles.container}>
      {title}
    </View>
  )
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff'
  }
})

export default Component
```

> Create React Native Screen Component

- `ddrnsc`

```tsx
import React from 'react'
import { View, StyleSheet, SafeAreaView } from 'react-native'
import { useNavigation } from '@react-navigation/native'

const ComponentScreen = () => {
  const navigation = useNavigation()

  return (
    <SafeAreaView style={styles.container}>
      <View style={styles.content}>
        {title}
      </View>
    </SafeAreaView>
  )
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff'
  },
  content: {
    flex: 1,
    padding: 16
  }
})

export default ComponentScreen
```

### Next.js Snippets

> Create Next.js App Router Page

- `ddnarp`

```tsx
import { NextPage } from 'next'

interface PageProps {
  title?: string
}

const Page: NextPage<PageProps> = ({}) => {
  return (
    <div></div>
  )
}

export default Page
```

> Create Next.js App Router Layout

- `ddnarl`

```tsx
import { NextPage, GetServerSideProps } from 'next'

interface LayoutProps {
  title?: string
}

const Layout: NextPage<LayoutProps> = ({}) => {
  return (
    <div></div>
  )
}

export const getServerSideProps: GetServerSideProps = async (ctx) => {
  return {
    props: {}
  }
}

export default Layout
```

> Create Next.js API Route

- `ddnar`

```tsx
import { NextPage, GetStaticProps } from 'next'

interface RouteProps {
  title?: string
}

const Route: NextPage<RouteProps> = ({}) => {
  return (
    <div></div>
  )
}

export const getStaticProps: GetStaticProps = async (ctx) => {
  return {
    props: {}
  }
}

export default Route
```

> Create Next.js Server Component

- `ddnsc`

```tsx
import { Metadata } from 'next'

export const metadata: Metadata = {
  title: 'Component',
  description: '${2:Page description}'
}

interface ComponentProps {
  title?: string
}

const Component = async ({ ${3:title} }: ComponentProps) => {
  return (
    <div>
      <h1>Component</h1>
      <div>
        /* Server component content */
      </div>
    </div>
  )
}

export default Component
```

> Create Next.js Client Component

- `ddncc`

```tsx
'use client'

import { useState, useEffect, useCallback } from 'react'

interface ComponentProps {
  title?: string,
  initialCount?: number
}

const Component = ({ title, initialCount = 0 }: ComponentProps) => {
  const [count, setCount] = useState(initialCount)
  const [isLoading, setIsLoading] = useState(false)

  const increment = useCallback(() => {
    setCount(prev => prev + 1)
  }, [count])

  const decrement = useCallback(() => {
    setCount(prev => prev - 1)
  }, [count])

  useEffect(() => {
    console.log('Client component mounted')
  }, [])
  return (
    <div>
      <h1>Component</h1>
      <div>
        <p>Count: {count}</p>
        <button onClick={increment} disabled={isLoading}>
          Increment
        </button>
        <button onClick={decrement} disabled={isLoading}>
          Decrement
        </button>
      </div>
    </div>
  )
}

export default Component
```

> Create Next.js Image Component

- `ddnic`

```tsx
export const getStaticProps: GetStaticProps = async (ctx) => {
  return {
    props: {}
  }
}

export default 
```

> Create Next.js Link Component

- `ddnlc`

```tsx
export const getStaticPaths: GetStaticPaths = async () => {
  return {
    paths: [],
    fallback: false
  }
}

export default getStaticPaths
```

> Create Next.js Initial Props

- `ddnip`

```tsx
${TM_FILENAME_BASE}.getInitialProps = async (ctx) => {
  return {
    props: {}
  }
}
```

> Create Next.js App

- `ddna`

```tsx
import type { AppProps } from 'next/app'

export default function MyApp({ Component, pageProps }: AppProps) {
  return <Component {...pageProps} />
}
```

> Create Next.js Document

- `ddnd`

```tsx
import Document, { Html, Head, Main, NextScript, DocumentContext } from 'next/document'

class MyDocument extends Document {
  static async getInitialProps(ctx: DocumentContext) {
    const initialProps = await Document.getInitialProps(ctx)
    return { ...initialProps }
  },

  render() {
    return (
      <Html>
        <Head />
        <body>
          <Main />
          <NextScript />
        </body>
      </Html>
    );
  }
}

export default MyDocument
```

> Create Next.js API Handler

- `ddnah`

```tsx
import type { NextApiRequest, NextApiResponse } from 'next'

interface ApiHandlerData {}

export default async function handler(req: NextApiRequest, res: NextApiResponse<ApiHandlerData>) {
  return res.status(200).json({})
}
```

> Create Next.js Middleware

- `ddnm`

```tsx
import { NextResponse } from 'next/server'
import type { NextRequest } from 'next/server'

export async function MyMiddlewareMiddleware(request: NextRequest) {
  return NextResponse.next()
}

export const config = {
  matcher: '/about/:path*'
}
```

## Usage

1. Open the file in VS Code (e.g. `.vue`, `.tsx`, `.js`, etc.)
2. Enter the prefix and press `Tab` or `Enter`

## License

MIT License

## 🙏 Thank you

This snippet collection was created to improve the productivity of developers. Please use it usefully!
