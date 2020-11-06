---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: ef369f67e683a214538f1ecb113f771e2f5cd2f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494664"
---
# <span data-ttu-id="8ce31-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="8ce31-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="8ce31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8ce31-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce31-103">Egy vagy több szolgáltatási szerkezet beállításainak hozzáadása vagy frissítése a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="8ce31-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ce31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8ce31-104">SYNTAX</span></span>

### <span data-ttu-id="8ce31-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="8ce31-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ce31-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="8ce31-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce31-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8ce31-107">DESCRIPTION</span></span>
<span data-ttu-id="8ce31-108">A **set-AzureRmServiceFabricSetting** használatával felveheti vagy frissítheti a szolgáltatás szerkezetének beállításait egy fürtben.</span><span class="sxs-lookup"><span data-stu-id="8ce31-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="8ce31-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8ce31-109">EXAMPLES</span></span>

### <span data-ttu-id="8ce31-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8ce31-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="8ce31-111">Ez a parancs "MaxFileOperationTimeout" értéket ad az "NamingService" szakasz alatti "5000" értékre.</span><span class="sxs-lookup"><span data-stu-id="8ce31-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="8ce31-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8ce31-112">PARAMETERS</span></span>

### <span data-ttu-id="8ce31-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8ce31-113">-Name</span></span>
<span data-ttu-id="8ce31-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="8ce31-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8ce31-115">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="8ce31-115">-Parameter</span></span>
<span data-ttu-id="8ce31-116">Paraméter.</span><span class="sxs-lookup"><span data-stu-id="8ce31-116">Parameter.</span></span>

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

### <span data-ttu-id="8ce31-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce31-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ce31-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ce31-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8ce31-119">-Szakasz</span><span class="sxs-lookup"><span data-stu-id="8ce31-119">-Section</span></span>
<span data-ttu-id="8ce31-120">Szakasz.</span><span class="sxs-lookup"><span data-stu-id="8ce31-120">Section.</span></span>

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

### <span data-ttu-id="8ce31-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="8ce31-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="8ce31-122">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="8ce31-122">Client authentication type.</span></span>

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

### <span data-ttu-id="8ce31-123">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="8ce31-123">-Value</span></span>
<span data-ttu-id="8ce31-124">Érték.</span><span class="sxs-lookup"><span data-stu-id="8ce31-124">Value.</span></span>

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

### <span data-ttu-id="8ce31-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8ce31-125">-Confirm</span></span>
<span data-ttu-id="8ce31-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8ce31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce31-127">-WhatIf</span></span>
<span data-ttu-id="8ce31-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8ce31-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ce31-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ce31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce31-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce31-130">-DefaultProfile</span></span>
<span data-ttu-id="8ce31-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ce31-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce31-132">CommonParameters</span></span>
<span data-ttu-id="8ce31-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8ce31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce31-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce31-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce31-135">INPUTS</span></span>

### <span data-ttu-id="8ce31-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8ce31-136">System.String</span></span>
<span data-ttu-id="8ce31-137">Microsoft. Azure. Command. ServiceFabric. models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="8ce31-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="8ce31-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ce31-138">OUTPUTS</span></span>

### <span data-ttu-id="8ce31-139">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="8ce31-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="8ce31-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8ce31-140">NOTES</span></span>

## <span data-ttu-id="8ce31-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ce31-141">RELATED LINKS</span></span>

