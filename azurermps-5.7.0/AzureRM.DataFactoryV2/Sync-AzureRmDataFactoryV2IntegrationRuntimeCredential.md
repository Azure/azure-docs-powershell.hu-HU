---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 11619cf9d5699b626032f82efbc9674713076ece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495407"
---
# <span data-ttu-id="fc179-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="fc179-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="fc179-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc179-102">SYNOPSIS</span></span>
<span data-ttu-id="fc179-103">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="fc179-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc179-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc179-104">SYNTAX</span></span>

### <span data-ttu-id="fc179-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc179-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc179-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc179-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc179-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fc179-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc179-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc179-108">DESCRIPTION</span></span>
<span data-ttu-id="fc179-109">A **szinkronizálás-AzureRmDataFactoryV2IntegrationRuntimeCredential** parancsmag a helyszíni hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között, így a hitelesítő adatok mindegyik csomópontban azonosak lesznek.</span><span class="sxs-lookup"><span data-stu-id="fc179-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="fc179-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fc179-110">EXAMPLES</span></span>

### <span data-ttu-id="fc179-111">Példa 1: integrációs futásidejű hitelesítő adatok szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="fc179-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="fc179-112">A parancsmag a hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="fc179-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="fc179-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc179-113">PARAMETERS</span></span>

### <span data-ttu-id="fc179-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fc179-114">-DataFactoryName</span></span>
<span data-ttu-id="fc179-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="fc179-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc179-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc179-116">-DefaultProfile</span></span>
<span data-ttu-id="fc179-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc179-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc179-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fc179-118">-Force</span></span>
<span data-ttu-id="fc179-119">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="fc179-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fc179-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc179-120">-InputObject</span></span>
<span data-ttu-id="fc179-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="fc179-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc179-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="fc179-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="fc179-123">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="fc179-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc179-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc179-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc179-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="fc179-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc179-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc179-126">-ResourceId</span></span>
<span data-ttu-id="fc179-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="fc179-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc179-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fc179-128">-Confirm</span></span>
<span data-ttu-id="fc179-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fc179-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc179-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc179-130">-WhatIf</span></span>
<span data-ttu-id="fc179-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fc179-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fc179-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc179-132">CommonParameters</span></span>
<span data-ttu-id="fc179-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc179-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc179-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc179-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc179-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc179-135">INPUTS</span></span>

### <span data-ttu-id="fc179-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fc179-136">System.String</span></span>
<span data-ttu-id="fc179-137">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fc179-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fc179-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc179-138">OUTPUTS</span></span>

### <span data-ttu-id="fc179-139">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="fc179-139">System.Object</span></span>

## <span data-ttu-id="fc179-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc179-140">NOTES</span></span>

## <span data-ttu-id="fc179-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc179-141">RELATED LINKS</span></span>

