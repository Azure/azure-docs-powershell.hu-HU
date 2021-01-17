---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345461"
---
# <span data-ttu-id="595b6-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="595b6-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="595b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595b6-102">SYNOPSIS</span></span>
<span data-ttu-id="595b6-103">Módosítsa a Service Fabric frissítési típusát a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="595b6-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="595b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="595b6-104">SYNTAX</span></span>

### <span data-ttu-id="595b6-105">Automatikus</span><span class="sxs-lookup"><span data-stu-id="595b6-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595b6-106">Kézi</span><span class="sxs-lookup"><span data-stu-id="595b6-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595b6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="595b6-107">DESCRIPTION</span></span>
<span data-ttu-id="595b6-108">A **Set-AzServiceFabricUpgradeType** típussal automatikus vagy manuális frissítési típust állíthat be adott Service Fabric-kódverzió esetén.</span><span class="sxs-lookup"><span data-stu-id="595b6-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="595b6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="595b6-109">EXAMPLES</span></span>

### <span data-ttu-id="595b6-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="595b6-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="595b6-111">Ezzel a paranccsal a fürt frissítési módját automatikusra állíthatja.</span><span class="sxs-lookup"><span data-stu-id="595b6-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="595b6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="595b6-112">PARAMETERS</span></span>

### <span data-ttu-id="595b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595b6-113">-DefaultProfile</span></span>
<span data-ttu-id="595b6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="595b6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="595b6-115">-Name</span></span>
<span data-ttu-id="595b6-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="595b6-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595b6-117">-ResourceGroupName</span></span>
<span data-ttu-id="595b6-118">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="595b6-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="595b6-119">-UpgradeMode</span></span>
<span data-ttu-id="595b6-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="595b6-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-121">-Version</span><span class="sxs-lookup"><span data-stu-id="595b6-121">-Version</span></span>
<span data-ttu-id="595b6-122">Fürtkód verziója</span><span class="sxs-lookup"><span data-stu-id="595b6-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="595b6-123">-Confirm</span></span>
<span data-ttu-id="595b6-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="595b6-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595b6-125">-WhatIf</span></span>
<span data-ttu-id="595b6-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="595b6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="595b6-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="595b6-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="595b6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595b6-128">CommonParameters</span></span>
<span data-ttu-id="595b6-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595b6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595b6-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="595b6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595b6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="595b6-131">INPUTS</span></span>

### <span data-ttu-id="595b6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="595b6-132">System.String</span></span>

### <span data-ttu-id="595b6-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="595b6-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="595b6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="595b6-134">OUTPUTS</span></span>

### <span data-ttu-id="595b6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="595b6-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="595b6-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="595b6-136">NOTES</span></span>

## <span data-ttu-id="595b6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="595b6-137">RELATED LINKS</span></span>
