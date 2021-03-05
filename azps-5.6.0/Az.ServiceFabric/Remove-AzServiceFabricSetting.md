---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 2df7c5f6af50bf581963f08e0544eb453f4b27df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005398"
---
# <span data-ttu-id="921c2-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="921c2-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="921c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="921c2-102">SYNOPSIS</span></span>
<span data-ttu-id="921c2-103">Távolítson el egy vagy több Service Fabric-beállítást a fürtből.</span><span class="sxs-lookup"><span data-stu-id="921c2-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="921c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="921c2-104">SYNTAX</span></span>

### <span data-ttu-id="921c2-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="921c2-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921c2-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="921c2-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921c2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="921c2-107">DESCRIPTION</span></span>
<span data-ttu-id="921c2-108">A **Remove-AzServiceFabricSetting segítségével** távolítsa el a Service Fabric beállításait a fürtből.</span><span class="sxs-lookup"><span data-stu-id="921c2-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="921c2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="921c2-109">EXAMPLES</span></span>

### <span data-ttu-id="921c2-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="921c2-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="921c2-111">Ez a parancs eltávolítja a "MaxCursors" beállításokat az "EseStore" szakaszban.</span><span class="sxs-lookup"><span data-stu-id="921c2-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="921c2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="921c2-112">PARAMETERS</span></span>

### <span data-ttu-id="921c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921c2-113">-DefaultProfile</span></span>
<span data-ttu-id="921c2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="921c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="921c2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="921c2-115">-Name</span></span>
<span data-ttu-id="921c2-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="921c2-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="921c2-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="921c2-117">-Parameter</span></span>
<span data-ttu-id="921c2-118">A szövetbeállítás paraméterneve</span><span class="sxs-lookup"><span data-stu-id="921c2-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="921c2-120">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="921c2-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="921c2-121">-Section</span><span class="sxs-lookup"><span data-stu-id="921c2-121">-Section</span></span>
<span data-ttu-id="921c2-122">A szövetbeállítás szakaszneve</span><span class="sxs-lookup"><span data-stu-id="921c2-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921c2-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="921c2-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="921c2-124">A szövetbeállítások tömbje</span><span class="sxs-lookup"><span data-stu-id="921c2-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="921c2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="921c2-125">-Confirm</span></span>
<span data-ttu-id="921c2-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="921c2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921c2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921c2-127">-WhatIf</span></span>
<span data-ttu-id="921c2-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="921c2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921c2-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="921c2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921c2-130">CommonParameters</span></span>
<span data-ttu-id="921c2-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="921c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921c2-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="921c2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921c2-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="921c2-133">INPUTS</span></span>

### <span data-ttu-id="921c2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="921c2-134">System.String</span></span>

### <span data-ttu-id="921c2-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="921c2-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="921c2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="921c2-136">OUTPUTS</span></span>

### <span data-ttu-id="921c2-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="921c2-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="921c2-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="921c2-138">NOTES</span></span>

## <span data-ttu-id="921c2-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="921c2-139">RELATED LINKS</span></span>
