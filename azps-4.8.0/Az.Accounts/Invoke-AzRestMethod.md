---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185115"
---
# <span data-ttu-id="b4f7d-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="b4f7d-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="b4f7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f7d-103">HTTP-kérés létesítése és végrehajtása csak az Azure erőforrás-kezelési végponttal</span><span class="sxs-lookup"><span data-stu-id="b4f7d-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="b4f7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4f7d-104">SYNTAX</span></span>

### <span data-ttu-id="b4f7d-105">ByPath (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4f7d-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4f7d-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="b4f7d-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f7d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4f7d-107">DESCRIPTION</span></span>
<span data-ttu-id="b4f7d-108">HTTP-kérés létesítése és végrehajtása csak az Azure erőforrás-kezelési végponttal</span><span class="sxs-lookup"><span data-stu-id="b4f7d-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="b4f7d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4f7d-109">EXAMPLES</span></span>

### <span data-ttu-id="b4f7d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4f7d-110">Example 1</span></span>
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

<span data-ttu-id="b4f7d-111">Log Analytics-munkaterület beolvasása elérésiút szerint</span><span class="sxs-lookup"><span data-stu-id="b4f7d-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="b4f7d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4f7d-112">PARAMETERS</span></span>

### <span data-ttu-id="b4f7d-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b4f7d-113">-ApiVersion</span></span>
<span data-ttu-id="b4f7d-114">API-verzió</span><span class="sxs-lookup"><span data-stu-id="b4f7d-114">Api Version</span></span>

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

### <span data-ttu-id="b4f7d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4f7d-115">-AsJob</span></span>
<span data-ttu-id="b4f7d-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="b4f7d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4f7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f7d-117">-DefaultProfile</span></span>
<span data-ttu-id="b4f7d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4f7d-119">-Módszer</span><span class="sxs-lookup"><span data-stu-id="b4f7d-119">-Method</span></span>
<span data-ttu-id="b4f7d-120">Http-módszer</span><span class="sxs-lookup"><span data-stu-id="b4f7d-120">Http Method</span></span>

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

### <span data-ttu-id="b4f7d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4f7d-121">-Name</span></span>
<span data-ttu-id="b4f7d-122">a cél erőforrás nevének listája</span><span class="sxs-lookup"><span data-stu-id="b4f7d-122">list of Target Resource Name</span></span>

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

### <span data-ttu-id="b4f7d-123">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="b4f7d-123">-Path</span></span>
<span data-ttu-id="b4f7d-124">Cél elérési útja</span><span class="sxs-lookup"><span data-stu-id="b4f7d-124">Target Path</span></span>

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

### <span data-ttu-id="b4f7d-125">-Hasznos teher</span><span class="sxs-lookup"><span data-stu-id="b4f7d-125">-Payload</span></span>
<span data-ttu-id="b4f7d-126">JSON formátumú adatforgalom</span><span class="sxs-lookup"><span data-stu-id="b4f7d-126">JSON format payload</span></span>

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

### <span data-ttu-id="b4f7d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f7d-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4f7d-128">Cél erőforrás csoport neve</span><span class="sxs-lookup"><span data-stu-id="b4f7d-128">Target Resource Group Name</span></span>

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

### <span data-ttu-id="b4f7d-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="b4f7d-129">-ResourceProviderName</span></span>
<span data-ttu-id="b4f7d-130">Cél erőforrás-szolgáltató neve</span><span class="sxs-lookup"><span data-stu-id="b4f7d-130">Target Resource Provider Name</span></span>

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

### <span data-ttu-id="b4f7d-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b4f7d-131">-ResourceType</span></span>
<span data-ttu-id="b4f7d-132">A cél erőforrás típusának listája</span><span class="sxs-lookup"><span data-stu-id="b4f7d-132">List of Target Resource Type</span></span>

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

### <span data-ttu-id="b4f7d-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4f7d-133">-SubscriptionId</span></span>
<span data-ttu-id="b4f7d-134">Cél-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="b4f7d-134">Target Subscription Id</span></span>

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

### <span data-ttu-id="b4f7d-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4f7d-135">-Confirm</span></span>
<span data-ttu-id="b4f7d-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f7d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f7d-137">-WhatIf</span></span>
<span data-ttu-id="b4f7d-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4f7d-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f7d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f7d-140">CommonParameters</span></span>
<span data-ttu-id="b4f7d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4f7d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f7d-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b4f7d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f7d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f7d-143">INPUTS</span></span>

### <span data-ttu-id="b4f7d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b4f7d-144">System.string</span></span>

## <span data-ttu-id="b4f7d-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f7d-145">OUTPUTS</span></span>

### <span data-ttu-id="b4f7d-146">Microsoft. Azure. Command. profil. models. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="b4f7d-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="b4f7d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4f7d-147">NOTES</span></span>

## <span data-ttu-id="b4f7d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4f7d-148">RELATED LINKS</span></span>
