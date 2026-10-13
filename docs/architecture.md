# Request Flow

## Create Issue

User → Frontend form → POST /api/issues → API validation → Data layer
      ← Render created issue ← 201 + JSON ←──────────────────┘ 
 
## View Issue

Page load → GET /api/issues → API → Data layer
 ← Render list ← 200 + JSON array ←───┘

## Update Issue

 Button → PATCH /api/issues/{id}/status → API validation → Data layer
         ← Re-render issue ← 200 + updated JSON ←──────────┘ 

# Trust Boundary

 USER-CONTROLLED SIDE               APPLICATION-CONTROLLED SIDE
Browser input ───── HTTP request ─────▶ REST API ─────▶ Data
▲                                      │
└────────── JSON response ◀────────────┘
