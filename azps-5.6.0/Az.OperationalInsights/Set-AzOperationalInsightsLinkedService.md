---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 141723a0e920f18aed9808ed3c5f205534c48185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937865"
---
# <span data-ttu-id="2514f-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="2514f-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="2514f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2514f-102">SYNOPSIS</span></span>
<span data-ttu-id="2514f-103">munkaterület-összekapcsolás-szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="2514f-103">link service for workspace</span></span>

## <span data-ttu-id="2514f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2514f-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2514f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2514f-105">DESCRIPTION</span></span>
<span data-ttu-id="2514f-106">munkaterület-összekapcsolás-szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="2514f-106">link service for workspace</span></span>

## <span data-ttu-id="2514f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2514f-107">EXAMPLES</span></span>

### <span data-ttu-id="2514f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2514f-108">Example 1</span></span>
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

<span data-ttu-id="2514f-109">munkaterület-összekapcsolás-fürt</span><span class="sxs-lookup"><span data-stu-id="2514f-109">link cluster for workspace</span></span>

## <span data-ttu-id="2514f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2514f-110">PARAMETERS</span></span>

### <span data-ttu-id="2514f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2514f-111">-AsJob</span></span>
<span data-ttu-id="2514f-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2514f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2514f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2514f-113">-DefaultProfile</span></span>
<span data-ttu-id="2514f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2514f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2514f-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="2514f-115">-LinkedServiceName</span></span>
<span data-ttu-id="2514f-116">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="2514f-116">The Workspace name.</span></span>

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

### <span data-ttu-id="2514f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2514f-117">-ResourceGroupName</span></span>
<span data-ttu-id="2514f-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2514f-118">The resource group name.</span></span>

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

### <span data-ttu-id="2514f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2514f-119">-ResourceId</span></span>
<span data-ttu-id="2514f-120">A munkaterülethez csatolva lévő erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2514f-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="2514f-121">Ezt olvasási hozzáférést igénylő erőforrások csatolása esetén érdemes használni.</span><span class="sxs-lookup"><span data-stu-id="2514f-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="2514f-122">-Címkék</span><span class="sxs-lookup"><span data-stu-id="2514f-122">-Tags</span></span>
<span data-ttu-id="2514f-123">Címkék.</span><span class="sxs-lookup"><span data-stu-id="2514f-123">Tags.</span></span>

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

### <span data-ttu-id="2514f-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2514f-124">-WorkspaceName</span></span>
<span data-ttu-id="2514f-125">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="2514f-125">The Workspace name.</span></span>

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

### <span data-ttu-id="2514f-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="2514f-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="2514f-127">A munkaterülethez csatolva lévő erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2514f-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="2514f-128">Ezt az írási hozzáférést igénylő erőforrások csatolása esetén érdemes használni.</span><span class="sxs-lookup"><span data-stu-id="2514f-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="2514f-129">A fürtnek rendelkeznie kell "Sikeres" kiépítési állapottal és érvényes kulcsbillentyű-tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="2514f-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="2514f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2514f-130">-Confirm</span></span>
<span data-ttu-id="2514f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2514f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2514f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2514f-132">-WhatIf</span></span>
<span data-ttu-id="2514f-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2514f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2514f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2514f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2514f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2514f-135">CommonParameters</span></span>
<span data-ttu-id="2514f-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2514f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2514f-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2514f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2514f-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2514f-138">INPUTS</span></span>

### <span data-ttu-id="2514f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2514f-139">System.String</span></span>

## <span data-ttu-id="2514f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2514f-140">OUTPUTS</span></span>

### <span data-ttu-id="2514f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2514f-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="2514f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2514f-142">NOTES</span></span>

## <span data-ttu-id="2514f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2514f-143">RELATED LINKS</span></span>
