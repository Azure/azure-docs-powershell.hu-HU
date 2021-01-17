---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469194"
---
# <span data-ttu-id="4e898-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="4e898-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="4e898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e898-102">SYNOPSIS</span></span>
<span data-ttu-id="4e898-103">Kizárólag Azure-erőforrás-kezelési végpontra vonatkozó HTTP-kérések építése és végrehajtása</span><span class="sxs-lookup"><span data-stu-id="4e898-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="4e898-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e898-104">SYNTAX</span></span>

### <span data-ttu-id="4e898-105">ByPath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e898-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e898-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="4e898-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e898-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e898-107">DESCRIPTION</span></span>
<span data-ttu-id="4e898-108">Kizárólag Azure-erőforrás-kezelési végpontra vonatkozó HTTP-kérések építése és végrehajtása</span><span class="sxs-lookup"><span data-stu-id="4e898-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="4e898-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e898-109">EXAMPLES</span></span>

### <span data-ttu-id="4e898-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4e898-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="4e898-111">Log analytics workspace by path</span><span class="sxs-lookup"><span data-stu-id="4e898-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="4e898-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e898-112">PARAMETERS</span></span>

### <span data-ttu-id="4e898-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4e898-113">-ApiVersion</span></span>
<span data-ttu-id="4e898-114">Api-verzió</span><span class="sxs-lookup"><span data-stu-id="4e898-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e898-115">-AsJob</span></span>
<span data-ttu-id="4e898-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4e898-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e898-117">-DefaultProfile</span></span>
<span data-ttu-id="4e898-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e898-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-119">-Method</span><span class="sxs-lookup"><span data-stu-id="4e898-119">-Method</span></span>
<span data-ttu-id="4e898-120">Http-módszer</span><span class="sxs-lookup"><span data-stu-id="4e898-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4e898-121">-Name</span></span>
<span data-ttu-id="4e898-122">List of Target Resource Name</span><span class="sxs-lookup"><span data-stu-id="4e898-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-123">-Path</span><span class="sxs-lookup"><span data-stu-id="4e898-123">-Path</span></span>
<span data-ttu-id="4e898-124">Cél elérési útja</span><span class="sxs-lookup"><span data-stu-id="4e898-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-125">-Hasznos terhelés</span><span class="sxs-lookup"><span data-stu-id="4e898-125">-Payload</span></span>
<span data-ttu-id="4e898-126">JSON formátum hasznos terhelése</span><span class="sxs-lookup"><span data-stu-id="4e898-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e898-127">-ResourceGroupName</span></span>
<span data-ttu-id="4e898-128">Célerőforrás-csoport neve</span><span class="sxs-lookup"><span data-stu-id="4e898-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="4e898-129">-ResourceProviderName</span></span>
<span data-ttu-id="4e898-130">Célerőforrás-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="4e898-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4e898-131">-ResourceType</span></span>
<span data-ttu-id="4e898-132">Célerőforrás-típus listája</span><span class="sxs-lookup"><span data-stu-id="4e898-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e898-133">-SubscriptionId</span></span>
<span data-ttu-id="4e898-134">Cél-előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="4e898-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e898-135">-Confirm</span></span>
<span data-ttu-id="4e898-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4e898-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e898-137">-WhatIf</span></span>
<span data-ttu-id="4e898-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4e898-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e898-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e898-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e898-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e898-140">CommonParameters</span></span>
<span data-ttu-id="4e898-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e898-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e898-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e898-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e898-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e898-143">INPUTS</span></span>

### <span data-ttu-id="4e898-144">System.string</span><span class="sxs-lookup"><span data-stu-id="4e898-144">System.string</span></span>

## <span data-ttu-id="4e898-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e898-145">OUTPUTS</span></span>

### <span data-ttu-id="4e898-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="4e898-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="4e898-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e898-147">NOTES</span></span>

## <span data-ttu-id="4e898-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e898-148">RELATED LINKS</span></span>
