---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024513"
---
# <span data-ttu-id="53303-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="53303-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="53303-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53303-102">SYNOPSIS</span></span>
<span data-ttu-id="53303-103">hivatkozás szolgáltatás a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="53303-103">link service for workspace</span></span>

## <span data-ttu-id="53303-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53303-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53303-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53303-105">DESCRIPTION</span></span>
<span data-ttu-id="53303-106">hivatkozás szolgáltatás a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="53303-106">link service for workspace</span></span>

## <span data-ttu-id="53303-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53303-107">EXAMPLES</span></span>

### <span data-ttu-id="53303-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="53303-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="53303-109">fürt csatolása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="53303-109">link cluster for workspace</span></span>

## <span data-ttu-id="53303-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53303-110">PARAMETERS</span></span>

### <span data-ttu-id="53303-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53303-111">-AsJob</span></span>
<span data-ttu-id="53303-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53303-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53303-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53303-113">-DefaultProfile</span></span>
<span data-ttu-id="53303-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53303-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53303-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="53303-115">-LinkedServiceName</span></span>
<span data-ttu-id="53303-116">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="53303-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53303-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53303-117">-ResourceGroupName</span></span>
<span data-ttu-id="53303-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="53303-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53303-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53303-119">-ResourceId</span></span>
<span data-ttu-id="53303-120">Annak az erőforrásnak az azonosítója, amely a munkaterülethez lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="53303-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="53303-121">Ezt a lehetőséget kell használni az olvasási hozzáférést igénylő erőforrások összekapcsolásához</span><span class="sxs-lookup"><span data-stu-id="53303-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="53303-122">-Címkék</span><span class="sxs-lookup"><span data-stu-id="53303-122">-Tags</span></span>
<span data-ttu-id="53303-123">Címkék.</span><span class="sxs-lookup"><span data-stu-id="53303-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53303-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53303-124">-WorkspaceName</span></span>
<span data-ttu-id="53303-125">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="53303-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53303-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="53303-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="53303-127">Annak az erőforrásnak az azonosítója, amely a munkaterülethez lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="53303-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="53303-128">Ezt a lehetőséget kell használni az írási hozzáférést igénylő erőforrások összekapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="53303-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="53303-129">A fürtnek rendelkeznie kell kiépítési állapotú "sikeres" és "érvényes" "beosztási" tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="53303-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="53303-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53303-130">-Confirm</span></span>
<span data-ttu-id="53303-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53303-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53303-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53303-132">-WhatIf</span></span>
<span data-ttu-id="53303-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53303-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53303-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53303-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53303-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53303-135">CommonParameters</span></span>
<span data-ttu-id="53303-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53303-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53303-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="53303-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53303-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53303-138">INPUTS</span></span>

### <span data-ttu-id="53303-139">System. String</span><span class="sxs-lookup"><span data-stu-id="53303-139">System.String</span></span>

## <span data-ttu-id="53303-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53303-140">OUTPUTS</span></span>

### <span data-ttu-id="53303-141">Microsoft. Azure. Command. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="53303-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="53303-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53303-142">NOTES</span></span>

## <span data-ttu-id="53303-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53303-143">RELATED LINKS</span></span>
