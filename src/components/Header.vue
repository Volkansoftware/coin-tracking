<template>
  <Popover class="relative transparent">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="flex justify-between items-center py-6 md:justify-start md:space-x-10">
        <div class="flex justify-start lg:w-0 lg:flex-1">
            <router-link class="text-white title" to="/"> COIN TRACKER</router-link>
        </div>
       
       
        <div class="hidden md:flex items-center justify-end md:flex-1 lg:w-0">
       
         <Popover class="relative " v-slot="{ open }">
            <PopoverButton   :class="[open ? 'text-gray-900 bgtransparent ' : 'text-gray-500', ' bgtransparent group bg-white rounded-md inline-flex items-center text-base font-medium hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500']">
              <span>Ana Sayfa</span>
              <ChevronDownIcon :class="[open ? 'text-gray-600' : 'text-gray-400', 'ml-2 h-5 w-5 group-hover:text-gray-500']" aria-hidden="true" />
            </PopoverButton>

            <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
              <PopoverPanel class="absolute z-10 left-1/2 transform translatePanel  mt-3 px-2 w-screen max-w-md sm:px-0">
                <div class="rounded-lg shadow-lg ring-1 ring-black ring-opacity-5 overflow-hidden">
                  <div class="relative grid gap-6 bg-white px-5 py-6 sm:gap-8 sm:p-8">
                    <router-link class="-m-3 p-3 flex items-start rounded-lg hover:bg-gray-50" :to="{name : 'About'}"> BTC</router-link>
                      <router-link class="-m-3 p-3 flex items-start rounded-lg hover:bg-gray-50" to="/"> Ana Sayfa</router-link>
                  </div>
               
                </div>
              </PopoverPanel>
            </transition>


          </Popover>
        </div>
      </div>
    </div>

    
  </Popover>
</template>

<script>
import { Popover, PopoverButton, PopoverGroup, PopoverPanel } from '@headlessui/vue'
import {
  BookmarkAltIcon,
  CalendarIcon,
  ChartBarIcon,
  CursorClickIcon,
  MenuIcon,
  PhoneIcon,
  PlayIcon,
  RefreshIcon,
  ShieldCheckIcon,
  SupportIcon,
  ViewGridIcon,
  XIcon,
} from '@heroicons/vue/outline'
import { ChevronDownIcon } from '@heroicons/vue/solid'

const solutions = [
  {
    name: 'Analytics',
    description: 'Get a better understanding of where your traffic is coming from.',
    href: '#',
    icon: ChartBarIcon,
  },
  {
    name: 'Engagement',
    description: 'Speak directly to your customers in a more meaningful way.',
    href: '#',
    icon: CursorClickIcon,
  },
  { name: 'Security', description: "Your customers' data will be safe and secure.", href: '#', icon: ShieldCheckIcon },
  {
    name: 'Integrations',
    description: "Connect with third-party tools that you're already using.",
    href: '#',
    icon: ViewGridIcon,
  },
  {
    name: 'Automations',
    description: 'Build strategic funnels that will drive your customers to convert',
    href: '#',
    icon: RefreshIcon,
  },
]
const callsToAction = [
  { name: 'Watch Demo', href: '#', icon: PlayIcon },
  { name: 'Contact Sales', href: '#', icon: PhoneIcon },
]
const resources = [
  {
    name: 'USD',
    
    href: '#',
    icon: SupportIcon,
  },
  {
    name: 'BTC',
  
    href: '#',
    icon: BookmarkAltIcon,
  },
  {
    name: 'Doge Coin',
  
    href: '#',
    icon: CalendarIcon,
  },
  { name: 'Etherium',  href: '#', icon: ShieldCheckIcon },
]
const recentPosts = [
  { id: 1, name: 'Boost your conversion rate', href: '#' },
  { id: 2, name: 'How to use search engine optimization to drive traffic to your site', href: '#' },
  { id: 3, name: 'Improve your customer experience', href: '#' },
]

export default {
  components: {
    Popover,
    PopoverButton,
    PopoverGroup,
    PopoverPanel,
    ChevronDownIcon,
    MenuIcon,
    XIcon,
   
  },
  setup() {
    return {
      solutions,
      callsToAction,
      resources,
      recentPosts,
    }
  },
}
</script>
<style>

.transparent{
  background-color: transparent;
}
.title{
  flex:1;
  color: gold !important;
  font-weight: bold;
  cursor: pointer;
}
.translatePanel{
transform: translateX(-69%) !important;
}
    
</style>