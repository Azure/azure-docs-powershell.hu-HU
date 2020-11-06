---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 42d643faa1b3047c6ee2e3266a68a2ce692ec676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497296"
---
# <span data-ttu-id="db858-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="db858-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="db858-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db858-102">SYNOPSIS</span></span>
<span data-ttu-id="db858-103">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="db858-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db858-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db858-104">SYNTAX</span></span>

### <span data-ttu-id="db858-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="db858-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db858-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="db858-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db858-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="db858-107">DESCRIPTION</span></span>
<span data-ttu-id="db858-108">A **set-AzureRmServiceFabricSetting** használatával felveheti vagy frissítheti a szolgáltatás szerkezetének beállításait egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="db858-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="db858-109">Példák</span><span class="sxs-lookup"><span data-stu-id="db858-109">EXAMPLES</span></span>

### <span data-ttu-id="db858-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db858-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="db858-111">Ez a parancs "MaxFileOperationTimeout" értéket ad az "NamingService" szakasz alatti "5000" értékre.</span><span class="sxs-lookup"><span data-stu-id="db858-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="db858-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db858-112">PARAMETERS</span></span>

### <span data-ttu-id="db858-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db858-113">-DefaultProfile</span></span>
<span data-ttu-id="db858-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db858-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db858-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db858-115">-Name</span></span>
<span data-ttu-id="db858-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="db858-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="db858-117">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="db858-117">-Parameter</span></span>
<span data-ttu-id="db858-118">Paraméter.</span><span class="sxs-lookup"><span data-stu-id="db858-118">Parameter.</span></span>

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

### <span data-ttu-id="db858-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db858-119">-ResourceGroupName</span></span>
<span data-ttu-id="db858-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db858-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="db858-121">-Szakasz</span><span class="sxs-lookup"><span data-stu-id="db858-121">-Section</span></span>
<span data-ttu-id="db858-122">Szakasz.</span><span class="sxs-lookup"><span data-stu-id="db858-122">Section.</span></span>

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

### <span data-ttu-id="db858-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="db858-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="db858-124">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="db858-124">Client authentication type.</span></span>

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

### <span data-ttu-id="db858-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="db858-125">-Value</span></span>
<span data-ttu-id="db858-126">Érték.</span><span class="sxs-lookup"><span data-stu-id="db858-126">Value.</span></span>

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

### <span data-ttu-id="db858-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db858-127">-Confirm</span></span>
<span data-ttu-id="db858-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db858-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db858-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db858-129">-WhatIf</span></span>
<span data-ttu-id="db858-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db858-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db858-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db858-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db858-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db858-132">CommonParameters</span></span>
<span data-ttu-id="db858-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db858-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db858-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db858-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db858-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db858-135">INPUTS</span></span>

### <span data-ttu-id="db858-136">System. String</span><span class="sxs-lookup"><span data-stu-id="db858-136">System.String</span></span>
<span data-ttu-id="db858-137">Paraméterek: paraméter (ByValue), Section (ByValue), Value (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db858-137">Parameters: Parameter (ByValue), Section (ByValue), Value (ByValue)</span></span>

### <span data-ttu-id="db858-138">Microsoft. Azure. Command. ServiceFabric. models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="db858-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="db858-139">Paraméterek: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="db858-139">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="db858-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db858-140">OUTPUTS</span></span>

### <span data-ttu-id="db858-141">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="db858-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="db858-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db858-142">NOTES</span></span>

## <span data-ttu-id="db858-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db858-143">RELATED LINKS</span></span>
