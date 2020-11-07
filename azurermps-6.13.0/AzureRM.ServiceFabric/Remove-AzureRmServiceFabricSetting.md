---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 4643ab29be9c93f58895048317edc2b1db6115e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679825"
---
# <span data-ttu-id="44891-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="44891-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="44891-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="44891-102">SYNOPSIS</span></span>
<span data-ttu-id="44891-103">Egy vagy több szolgáltatási anyag beállítás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="44891-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44891-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="44891-104">SYNTAX</span></span>

### <span data-ttu-id="44891-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="44891-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44891-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="44891-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44891-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="44891-107">DESCRIPTION</span></span>
<span data-ttu-id="44891-108">Távolítsa el a **AzureRmServiceFabricSetting** a Service Fabric beállításaiból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="44891-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="44891-109">Példák</span><span class="sxs-lookup"><span data-stu-id="44891-109">EXAMPLES</span></span>

### <span data-ttu-id="44891-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="44891-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="44891-111">Ez a parancs eltávolítja a beállítások "MaxCursors" nevű "EseStore" szakaszát.</span><span class="sxs-lookup"><span data-stu-id="44891-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="44891-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="44891-112">PARAMETERS</span></span>

### <span data-ttu-id="44891-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44891-113">-DefaultProfile</span></span>
<span data-ttu-id="44891-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44891-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44891-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="44891-115">-Name</span></span>
<span data-ttu-id="44891-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="44891-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="44891-117">-Paraméter</span><span class="sxs-lookup"><span data-stu-id="44891-117">-Parameter</span></span>
<span data-ttu-id="44891-118">Paraméter.</span><span class="sxs-lookup"><span data-stu-id="44891-118">Parameter.</span></span>

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

### <span data-ttu-id="44891-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44891-119">-ResourceGroupName</span></span>
<span data-ttu-id="44891-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="44891-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="44891-121">-Szakasz</span><span class="sxs-lookup"><span data-stu-id="44891-121">-Section</span></span>
<span data-ttu-id="44891-122">Szakasz.</span><span class="sxs-lookup"><span data-stu-id="44891-122">Section.</span></span>

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

### <span data-ttu-id="44891-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="44891-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="44891-124">Ügyfél-hitelesítés típusa</span><span class="sxs-lookup"><span data-stu-id="44891-124">Client authentication type.</span></span>

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

### <span data-ttu-id="44891-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="44891-125">-Confirm</span></span>
<span data-ttu-id="44891-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44891-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44891-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44891-127">-WhatIf</span></span>
<span data-ttu-id="44891-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="44891-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44891-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44891-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44891-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44891-130">CommonParameters</span></span>
<span data-ttu-id="44891-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="44891-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44891-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44891-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44891-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="44891-133">INPUTS</span></span>

### <span data-ttu-id="44891-134">System. String</span><span class="sxs-lookup"><span data-stu-id="44891-134">System.String</span></span>
<span data-ttu-id="44891-135">Paraméterek: paraméter (ByValue), szakasz (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44891-135">Parameters: Parameter (ByValue), Section (ByValue)</span></span>

### <span data-ttu-id="44891-136">Microsoft. Azure. Command. ServiceFabric. models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="44891-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="44891-137">Paraméterek: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44891-137">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="44891-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44891-138">OUTPUTS</span></span>

### <span data-ttu-id="44891-139">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="44891-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="44891-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="44891-140">NOTES</span></span>

## <span data-ttu-id="44891-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44891-141">RELATED LINKS</span></span>
