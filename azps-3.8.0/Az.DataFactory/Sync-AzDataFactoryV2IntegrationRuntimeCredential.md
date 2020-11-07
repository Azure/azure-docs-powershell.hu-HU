---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: cb9362a64b58770beb7d3b70f989fc740a2fc00e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847081"
---
# <span data-ttu-id="4c0e0-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="4c0e0-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="4c0e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0e0-103">Szinkronizálja a hitelesítő adatokat az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="4c0e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c0e0-104">SYNTAX</span></span>

### <span data-ttu-id="4c0e0-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4c0e0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c0e0-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0e0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4c0e0-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c0e0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c0e0-108">DESCRIPTION</span></span>
<span data-ttu-id="4c0e0-109">A **szinkronizálás-AzDataFactoryV2IntegrationRuntimeCredential** parancsmag a helyszíni hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között, így a hitelesítő adatok mindegyik csomópontban azonosak lesznek.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="4c0e0-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4c0e0-110">EXAMPLES</span></span>

### <span data-ttu-id="4c0e0-111">Példa 1: integrációs futásidejű hitelesítő adatok szinkronizálása</span><span class="sxs-lookup"><span data-stu-id="4c0e0-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="4c0e0-112">A parancsmag a hitelesítő adatokat szinkronizálja az integrációs futásidejű csomópontok között.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="4c0e0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c0e0-113">PARAMETERS</span></span>

### <span data-ttu-id="4c0e0-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4c0e0-114">-DataFactoryName</span></span>
<span data-ttu-id="4c0e0-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0e0-116">-DefaultProfile</span></span>
<span data-ttu-id="4c0e0-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c0e0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4c0e0-118">-Force</span></span>
<span data-ttu-id="4c0e0-119">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c0e0-120">-InputObject</span></span>
<span data-ttu-id="4c0e0-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e0-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4c0e0-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="4c0e0-123">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c0e0-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c0e0-126">-ResourceId</span></span>
<span data-ttu-id="4c0e0-127">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0e0-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4c0e0-128">-Confirm</span></span>
<span data-ttu-id="4c0e0-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c0e0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0e0-130">-WhatIf</span></span>
<span data-ttu-id="4c0e0-131">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4c0e0-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4c0e0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0e0-132">CommonParameters</span></span>
<span data-ttu-id="4c0e0-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c0e0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0e0-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0e0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0e0-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c0e0-135">INPUTS</span></span>

### <span data-ttu-id="4c0e0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4c0e0-136">System.String</span></span>

### <span data-ttu-id="4c0e0-137">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4c0e0-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4c0e0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c0e0-138">OUTPUTS</span></span>

### <span data-ttu-id="4c0e0-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="4c0e0-139">System.Void</span></span>

## <span data-ttu-id="4c0e0-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c0e0-140">NOTES</span></span>

## <span data-ttu-id="4c0e0-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c0e0-141">RELATED LINKS</span></span>
