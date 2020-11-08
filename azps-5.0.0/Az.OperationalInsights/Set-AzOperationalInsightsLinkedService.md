---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188078"
---
# <span data-ttu-id="353a1-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="353a1-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="353a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="353a1-102">SYNOPSIS</span></span>
<span data-ttu-id="353a1-103">hivatkozás szolgáltatás a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="353a1-103">link service for workspace</span></span>

## <span data-ttu-id="353a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="353a1-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="353a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="353a1-105">DESCRIPTION</span></span>
<span data-ttu-id="353a1-106">hivatkozás szolgáltatás a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="353a1-106">link service for workspace</span></span>

## <span data-ttu-id="353a1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="353a1-107">EXAMPLES</span></span>

### <span data-ttu-id="353a1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="353a1-108">Example 1</span></span>
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

<span data-ttu-id="353a1-109">fürt csatolása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="353a1-109">link cluster for workspace</span></span>

## <span data-ttu-id="353a1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="353a1-110">PARAMETERS</span></span>

### <span data-ttu-id="353a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="353a1-111">-AsJob</span></span>
<span data-ttu-id="353a1-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="353a1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="353a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353a1-113">-DefaultProfile</span></span>
<span data-ttu-id="353a1-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="353a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="353a1-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="353a1-115">-LinkedServiceName</span></span>
<span data-ttu-id="353a1-116">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="353a1-116">The Workspace name.</span></span>

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

### <span data-ttu-id="353a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="353a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="353a1-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="353a1-118">The resource group name.</span></span>

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

### <span data-ttu-id="353a1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="353a1-119">-ResourceId</span></span>
<span data-ttu-id="353a1-120">Annak az erőforrásnak az azonosítója, amely a munkaterülethez lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="353a1-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="353a1-121">Ezt a lehetőséget kell használni az olvasási hozzáférést igénylő erőforrások összekapcsolásához</span><span class="sxs-lookup"><span data-stu-id="353a1-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="353a1-122">-Címkék</span><span class="sxs-lookup"><span data-stu-id="353a1-122">-Tags</span></span>
<span data-ttu-id="353a1-123">Címkék.</span><span class="sxs-lookup"><span data-stu-id="353a1-123">Tags.</span></span>

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

### <span data-ttu-id="353a1-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="353a1-124">-WorkspaceName</span></span>
<span data-ttu-id="353a1-125">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="353a1-125">The Workspace name.</span></span>

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

### <span data-ttu-id="353a1-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="353a1-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="353a1-127">Annak az erőforrásnak az azonosítója, amely a munkaterülethez lesz társítva.</span><span class="sxs-lookup"><span data-stu-id="353a1-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="353a1-128">Ezt a lehetőséget kell használni az írási hozzáférést igénylő erőforrások összekapcsolásához.</span><span class="sxs-lookup"><span data-stu-id="353a1-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="353a1-129">A fürtnek rendelkeznie kell kiépítési állapotú "sikeres" és "érvényes" "beosztási" tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="353a1-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="353a1-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="353a1-130">-Confirm</span></span>
<span data-ttu-id="353a1-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="353a1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="353a1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="353a1-132">-WhatIf</span></span>
<span data-ttu-id="353a1-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="353a1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="353a1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="353a1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="353a1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353a1-135">CommonParameters</span></span>
<span data-ttu-id="353a1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="353a1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353a1-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="353a1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353a1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="353a1-138">INPUTS</span></span>

### <span data-ttu-id="353a1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="353a1-139">System.String</span></span>

## <span data-ttu-id="353a1-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="353a1-140">OUTPUTS</span></span>

### <span data-ttu-id="353a1-141">Microsoft. Azure. Command. OperationalInsights. models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="353a1-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="353a1-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="353a1-142">NOTES</span></span>

## <span data-ttu-id="353a1-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="353a1-143">RELATED LINKS</span></span>
