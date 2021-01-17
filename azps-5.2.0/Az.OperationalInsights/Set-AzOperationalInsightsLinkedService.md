---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348138"
---
# <span data-ttu-id="21450-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="21450-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="21450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21450-102">SYNOPSIS</span></span>
<span data-ttu-id="21450-103">munkaterület-összekapcsolás-szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="21450-103">link service for workspace</span></span>

## <span data-ttu-id="21450-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21450-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21450-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21450-105">DESCRIPTION</span></span>
<span data-ttu-id="21450-106">munkaterület-összekapcsolás-szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="21450-106">link service for workspace</span></span>

## <span data-ttu-id="21450-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21450-107">EXAMPLES</span></span>

### <span data-ttu-id="21450-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="21450-108">Example 1</span></span>
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

<span data-ttu-id="21450-109">munkaterület-összekapcsolás-fürt</span><span class="sxs-lookup"><span data-stu-id="21450-109">link cluster for workspace</span></span>

## <span data-ttu-id="21450-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21450-110">PARAMETERS</span></span>

### <span data-ttu-id="21450-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21450-111">-AsJob</span></span>
<span data-ttu-id="21450-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="21450-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21450-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21450-113">-DefaultProfile</span></span>
<span data-ttu-id="21450-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21450-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21450-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="21450-115">-LinkedServiceName</span></span>
<span data-ttu-id="21450-116">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="21450-116">The Workspace name.</span></span>

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

### <span data-ttu-id="21450-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21450-117">-ResourceGroupName</span></span>
<span data-ttu-id="21450-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="21450-118">The resource group name.</span></span>

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

### <span data-ttu-id="21450-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21450-119">-ResourceId</span></span>
<span data-ttu-id="21450-120">A munkaterülethez csatolva lévő erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="21450-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="21450-121">Ezt olvasási hozzáférést igénylő erőforrások csatolása esetén érdemes használni.</span><span class="sxs-lookup"><span data-stu-id="21450-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="21450-122">-Címkék</span><span class="sxs-lookup"><span data-stu-id="21450-122">-Tags</span></span>
<span data-ttu-id="21450-123">Címkék.</span><span class="sxs-lookup"><span data-stu-id="21450-123">Tags.</span></span>

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

### <span data-ttu-id="21450-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21450-124">-WorkspaceName</span></span>
<span data-ttu-id="21450-125">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="21450-125">The Workspace name.</span></span>

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

### <span data-ttu-id="21450-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="21450-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="21450-127">A munkaterülethez csatolva lévő erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="21450-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="21450-128">Ezt az írási hozzáférést igénylő erőforrások csatolása esetén érdemes használni.</span><span class="sxs-lookup"><span data-stu-id="21450-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="21450-129">A fürtnek rendelkeznie kell "Sikeres" kiépítési állapottal és érvényes kulcsbillentyű-tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="21450-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="21450-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21450-130">-Confirm</span></span>
<span data-ttu-id="21450-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="21450-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21450-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21450-132">-WhatIf</span></span>
<span data-ttu-id="21450-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="21450-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21450-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21450-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21450-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21450-135">CommonParameters</span></span>
<span data-ttu-id="21450-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21450-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21450-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21450-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21450-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21450-138">INPUTS</span></span>

### <span data-ttu-id="21450-139">System.String</span><span class="sxs-lookup"><span data-stu-id="21450-139">System.String</span></span>

## <span data-ttu-id="21450-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21450-140">OUTPUTS</span></span>

### <span data-ttu-id="21450-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="21450-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="21450-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21450-142">NOTES</span></span>

## <span data-ttu-id="21450-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21450-143">RELATED LINKS</span></span>
