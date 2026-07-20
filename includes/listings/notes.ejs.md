```{=html}
<div class="academic-listing academic-listing-notes list">
<% for (const item of items) { 
     const updated = item['date-modified'] || item.date;
     const categories = item.categories || [];
%>
  <article class="academic-entry academic-entry-note" <%= metadataAttrs(item) %>>
    <div class="academic-entry-topline">
      <div class="academic-entry-meta">
        <% if (updated) { %>
          <span class="academic-entry-date listing-date-modified">
            <i class="bi bi-clock" aria-hidden="true"></i>
            Updated <%- updated %>
          </span>
        <% } %>
        <% if (item.status) { %>
          <span class="academic-entry-status listing-status"><%- item.status %></span>
        <% } %>
        <% if (item['reading-time']) { %>
          <span class="academic-entry-reading listing-reading-time"><%- item['reading-time'] %></span>
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
