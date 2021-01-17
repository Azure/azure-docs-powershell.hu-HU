---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362471"
---
# <span data-ttu-id="afca4-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="afca4-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="afca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afca4-102">SYNOPSIS</span></span>
<span data-ttu-id="afca4-103">Vegyen fel vagy frissítsen egy vagy több Service Fabric-beállítást a fürtben.</span><span class="sxs-lookup"><span data-stu-id="afca4-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="afca4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="afca4-104">SYNTAX</span></span>

### <span data-ttu-id="afca4-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="afca4-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afca4-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="afca4-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afca4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="afca4-107">DESCRIPTION</span></span>
<span data-ttu-id="afca4-108">A **Set-AzServiceFabricSetting segítségével** hozzáadhatja vagy frissítheti a Service Fabric beállításait egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="afca4-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="afca4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="afca4-109">EXAMPLES</span></span>

### <span data-ttu-id="afca4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="afca4-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="afca4-111">Ez a parancs a "MaxFileOperationTimeout" értéket "5000" értékre fogja állítani az "NamingService" szakaszban.</span><span class="sxs-lookup"><span data-stu-id="afca4-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="afca4-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="afca4-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="afca4-113">Ez a parancs elindít egy frissítést, amely a SettingsSectionDescription paraméterrel több szövetbeállítást is beállít.</span><span class="sxs-lookup"><span data-stu-id="afca4-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="afca4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afca4-114">PARAMETERS</span></span>

### <span data-ttu-id="afca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afca4-115">-DefaultProfile</span></span>
<span data-ttu-id="afca4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afca4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afca4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="afca4-117">-Name</span></span>
<span data-ttu-id="afca4-118">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="afca4-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="afca4-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="afca4-119">-Parameter</span></span>
<span data-ttu-id="afca4-120">A szövetbeállítás paraméterneve</span><span class="sxs-lookup"><span data-stu-id="afca4-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="afca4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afca4-121">-ResourceGroupName</span></span>
<span data-ttu-id="afca4-122">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="afca4-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="afca4-123">-Section</span><span class="sxs-lookup"><span data-stu-id="afca4-123">-Section</span></span>
<span data-ttu-id="afca4-124">A szövetbeállítás szakaszneve</span><span class="sxs-lookup"><span data-stu-id="afca4-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="afca4-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="afca4-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="afca4-126">A szövetbeállítások tömbje</span><span class="sxs-lookup"><span data-stu-id="afca4-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="afca4-127">-Érték</span><span class="sxs-lookup"><span data-stu-id="afca4-127">-Value</span></span>
<span data-ttu-id="afca4-128">A szövetbeállítás paraméterértéke</span><span class="sxs-lookup"><span data-stu-id="afca4-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="afca4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afca4-129">-Confirm</span></span>
<span data-ttu-id="afca4-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="afca4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afca4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afca4-131">-WhatIf</span></span>
<span data-ttu-id="afca4-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="afca4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afca4-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="afca4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afca4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afca4-134">CommonParameters</span></span>
<span data-ttu-id="afca4-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afca4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afca4-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afca4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afca4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afca4-137">INPUTS</span></span>

### <span data-ttu-id="afca4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="afca4-138">System.String</span></span>

### <span data-ttu-id="afca4-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="afca4-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="afca4-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afca4-140">OUTPUTS</span></span>

### <span data-ttu-id="afca4-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="afca4-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="afca4-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="afca4-142">NOTES</span></span>

## <span data-ttu-id="afca4-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afca4-143">RELATED LINKS</span></span>
