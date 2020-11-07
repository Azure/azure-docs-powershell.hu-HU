---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672225"
---
# <span data-ttu-id="c800a-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="c800a-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="c800a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c800a-102">SYNOPSIS</span></span>
<span data-ttu-id="c800a-103">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="c800a-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c800a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c800a-104">SYNTAX</span></span>

### <span data-ttu-id="c800a-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c800a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c800a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c800a-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c800a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c800a-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c800a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c800a-108">DESCRIPTION</span></span>
<span data-ttu-id="c800a-109">A **szinkronizálás-AzureRmDataFactoryV2IntegrationRuntimeCredential** parancsmag a helyszíni hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között, így a hitelesítő adatok mindegyik csomópontban azonosak lesznek.</span><span class="sxs-lookup"><span data-stu-id="c800a-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="c800a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c800a-110">EXAMPLES</span></span>

### <span data-ttu-id="c800a-111">Példa 1: integrációs futásidejű hitelesítő adatok szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="c800a-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="c800a-112">A parancsmag a hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="c800a-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="c800a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c800a-113">PARAMETERS</span></span>

### <span data-ttu-id="c800a-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c800a-114">-Confirm</span></span>
<span data-ttu-id="c800a-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c800a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c800a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c800a-116">-DataFactoryName</span></span>
<span data-ttu-id="c800a-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c800a-117">The data factory name.</span></span>

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

### <span data-ttu-id="c800a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c800a-118">-Force</span></span>
<span data-ttu-id="c800a-119">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c800a-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c800a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c800a-120">-InputObject</span></span>
<span data-ttu-id="c800a-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="c800a-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="c800a-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c800a-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c800a-123">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="c800a-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="c800a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c800a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c800a-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c800a-125">The resource group name.</span></span>

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

### <span data-ttu-id="c800a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c800a-126">-ResourceId</span></span>
<span data-ttu-id="c800a-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c800a-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c800a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c800a-128">-WhatIf</span></span>
<span data-ttu-id="c800a-129">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c800a-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="c800a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c800a-130">INPUTS</span></span>

### <span data-ttu-id="c800a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c800a-131">System.String</span></span>
<span data-ttu-id="c800a-132">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c800a-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="c800a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c800a-133">OUTPUTS</span></span>

### <span data-ttu-id="c800a-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c800a-134">System.Object</span></span>

## <span data-ttu-id="c800a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c800a-135">NOTES</span></span>

## <span data-ttu-id="c800a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c800a-136">RELATED LINKS</span></span>
