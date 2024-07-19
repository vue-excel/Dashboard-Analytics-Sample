<script setup lang="ts">
import { ref } from 'vue'
import BreadcrumbDefault from '@/components/Breadcrumbs/BreadcrumbDefault.vue'
import CalendarCard from '@/components/CalendarCard.vue'
import DefaultLayout from '@/layouts/DefaultLayout.vue'


const pageTitle = ref('Calender')
const activeDiv = ref(1)

const showDiv = (index: number) => {
  activeDiv.value = index
}
</script>

<template>
  <DefaultLayout>
    <div class="mx-auto max-w-7xl">
      <div class="analytics">
      <div @click="showDiv(1)" class="button"><h3>MarketPlace 1</h3></div>
      <div @click="showDiv(2)" class="button"><h3>MarketPlace 2</h3></div>
      <div @click="showDiv(3)" class="button"><h3>MarketPlace 3</h3></div>
      <div @click="showDiv(4)" class="button"><h3>MarketPlace 4</h3></div>
      <div @click="showDiv(5)" class="button"><h3>MarketPlace 5</h3></div>
    </div>
      
      <!-- Conditionally render divs based on activeDiv -->
      <div v-if="activeDiv === 1" class="card">
        <h2>Welcome to MarketPlace 1</h2>
  <p>Discover the latest trends and insights in our marketplace.</p>
  <ul>
    <li>Trend Analysis</li>
    <li>Customer Insights</li>
    <li>Sales Performance</li>
    <li>Product Reviews</li>
  </ul>
  <button @click="exploreMore">Explore More</button>
      </div>
        <div v-if="activeDiv === 2" class="card">
  <h2>Welcome to MarketPlace 2</h2>
  <p>Get in-depth analytics and reports for MarketPlace 2.</p>
  <ul>
    <li>Revenue Statistics</li>
    <li>Top Performing Products</li>
    <li>Customer Demographics</li>
    <li>Market Share Analysis</li>
  </ul>
  <button @click="viewDetails">View Details</button>
      </div>
      <div v-if="activeDiv === 3" class="card">
  <h2>Welcome to MarketPlace 3</h2>
  <p>Explore comprehensive insights and analytics for MarketPlace 3.</p>
  <div class="statistics">
    <div>
      <h3>Key Metrics</h3>
      <p>Total Sales: $2,500,000</p>
      <p>Active Users: 12,340</p>
    </div>
    <div>
      <h3>Recent Trends</h3>
      <p>Latest Growth Rate: 5.8%</p>
      <p>Top Selling Category: Electronics</p>
    </div>
  </div>
  <button @click="showMoreInfo">Show More Info</button>
</div>
<div v-if="activeDiv === 4" class="card">
  <h2>Welcome to MarketPlace 4</h2>
  <p>Detailed analysis and insights for MarketPlace 4.</p>
  <section class="overview">
    <h3>Highlights</h3>
    <p>Total Transactions: 7,890</p>
    <p>Average Order Value: $120</p>
    <p>Customer Satisfaction: 89%</p>
  </section>
  <section class="recent-activity">
    <h3>Recent Activity</h3>
    <ul>
      <li>New Feature Launched: Wishlist Integration</li>
      <li>Promotional Campaign: Summer Sale</li>
      <li>Customer Feedback: Increased Positive Reviews</li>
    </ul>
  </section>
  <button @click="getDetailedReport">Get Detailed Report</button>
</div>
<div v-if="activeDiv === 5" class="card">
  <h2>Welcome to MarketPlace 5</h2>
  <p>In-depth performance metrics and insights for MarketPlace 5.</p>
  <div class="performance">
    <div class="metric">
      <h3>Performance Metrics</h3>
      <p>Total Revenue: $3,200,000</p>
      <p>Number of Orders: 15,500</p>
      <p>Return Rate: 2.5%</p>
    </div>
    <div class="trends">
      <h3>Trends</h3>
      <p>Top Performing Region: North America</p>
      <p>Fastest Growing Category: Home Appliances</p>
      <p>Customer Retention Rate: 78%</p>
    </div>
  </div>
  <button @click="generateReport">Generate Report</button>
</div>
      
      <!-- Breadcrumb Start -->
      <!-- <BreadcrumbDefault :pageTitle="pageTitle" /> -->
      <!-- Breadcrumb End -->
      <!-- <CalendarCard /> -->
    </div>
  </DefaultLayout>
</template>

<style>
.analytics {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  color: red;
  border: 1px solid gray;
  padding: 8px;
  border-radius: 10px;
}
h3 {
  cursor: pointer;
}
.button {
  cursor: pointer;
  padding: 10px;
  border: 1px solid #363131;
  border-radius: 8px;
  transition: background-color 0.3s;
  background-color: white;
}
.button:hover {
  background-color: #181515;
  color:white;
}
.card {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 20px;
  margin-top: 10px;
  background-color:#fff;
  color: #444;
}
h2{
  text-align: center;
  font-size: 22px;
  margin-bottom: 8px;
  font-weight: 600;
}
</style>
