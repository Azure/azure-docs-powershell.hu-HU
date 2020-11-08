---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 72a538c039914eebdcd2926cda93a97cfe2d267a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187530"
---
# <span data-ttu-id="a931b-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a931b-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="a931b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a931b-102">SYNOPSIS</span></span>
<span data-ttu-id="a931b-103">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="a931b-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="a931b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a931b-104">SYNTAX</span></span>

### <span data-ttu-id="a931b-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="a931b-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a931b-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="a931b-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a931b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a931b-107">DESCRIPTION</span></span>
<span data-ttu-id="a931b-108">A **set-AzServiceFabricSetting** használatával felveheti vagy frissítheti a szolgáltatás szerkezetének beállításait egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="a931b-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="a931b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a931b-109">EXAMPLES</span></span>

### <span data-ttu-id="a931b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a931b-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="a931b-111">Ez a parancs "MaxFileOperationTimeout" értéket ad az "NamingService" szakasz alatti "5000" értékre.</span><span class="sxs-lookup"><span data-stu-id="a931b-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="a931b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a931b-112">PARAMETERS</span></span>

### <span data-ttu-id="a931b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a931b-113">-DefaultProfile</span></span>
<span data-ttu-id="a931b-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a931b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a931b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a931b-115">-Name</span></span>
<span data-ttu-id="a931b-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="a931b-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a931b-117">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="a931b-117">-Parameter</span></span>
<span data-ttu-id="a931b-118">A szövet beállítás paraméterének neve</span><span class="sxs-lookup"><span data-stu-id="a931b-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="a931b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a931b-119">-ResourceGroupName</span></span>
<span data-ttu-id="a931b-120">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="a931b-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a931b-121">-Szakasz</span><span class="sxs-lookup"><span data-stu-id="a931b-121">-Section</span></span>
<span data-ttu-id="a931b-122">A szövet beállításának szakasz neve</span><span class="sxs-lookup"><span data-stu-id="a931b-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="a931b-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="a931b-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="a931b-124">A szövet beállításainak tömbje</span><span class="sxs-lookup"><span data-stu-id="a931b-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="a931b-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="a931b-125">-Value</span></span>
<span data-ttu-id="a931b-126">A szövet beállítás paramétereinek értéke</span><span class="sxs-lookup"><span data-stu-id="a931b-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="a931b-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a931b-127">-Confirm</span></span>
<span data-ttu-id="a931b-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a931b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a931b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a931b-129">-WhatIf</span></span>
<span data-ttu-id="a931b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a931b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a931b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a931b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a931b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a931b-132">CommonParameters</span></span>
<span data-ttu-id="a931b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a931b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a931b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a931b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a931b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a931b-135">INPUTS</span></span>

### <span data-ttu-id="a931b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a931b-136">System.String</span></span>

### <span data-ttu-id="a931b-137">Microsoft. Azure. Command. ServiceFabric. models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="a931b-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="a931b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a931b-138">OUTPUTS</span></span>

### <span data-ttu-id="a931b-139">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a931b-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a931b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a931b-140">NOTES</span></span>

## <span data-ttu-id="a931b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a931b-141">RELATED LINKS</span></span>
