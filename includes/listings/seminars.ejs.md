```{=html}
<div class="academic-listing academic-listing-records list">
<% for (const item of items) { 
     const categories = item.categories || [];
%>
  <article class="academic-entry academic-entry-record" <%= metadataAttrs(item) %>>
    <div class="academic-entry-topline">
      <div class="academic-entry-meta">
        <% if (item.date) { %>
          <span class="academic-entry-date listing-date">
            <i class="bi bi-calendar3" aria-hidden="true"></i>
            <%- item.date %>
          </span>
        <% } %>
        <% if (item.status) { %>
          <span class="academic-entry-status listing-status"><%- item.status %></span>
        <% } %>
      </div>
      <a class="academic-entry-arrow" href="<%- item.path %>" aria-label="Open <%- item.title %>">
        <i class="bi bi-arrow-up-right" aria-hidden="true"></i>
      </a>
    </div>

    <h3 class="academic-entry-title">
      <a href="<%- item.path %>" class="listing-title"><%- item.title %></a>
    </h3>

    <% if (item.description) { %>
      <p class="academic-entry-description listing-description"><%- item.description %></p>
    <% } %>

    <% if (categories.length > 0) { %>
      <div class="academic-tags listing-categories">
        <% for (const category of categories) { %>
          <span class="academic-tag"><%- category %></span>
        <% } %>
      </div>
    <% } %>
  </article>
<% } %>
</div>
```
