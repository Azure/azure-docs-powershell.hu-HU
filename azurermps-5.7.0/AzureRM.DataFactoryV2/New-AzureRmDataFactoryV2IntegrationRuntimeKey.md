---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2ac4868905ee1de93f87ecb17d6b9ced0f036cda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492311"
---
# <span data-ttu-id="b0dc3-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="b0dc3-101">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="b0dc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dc3-103">Önkiszolgáló integrációs futásidejű kulcs újbóli létrehozása</span><span class="sxs-lookup"><span data-stu-id="b0dc3-103">Regenerate self-hosted integration runtime key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0dc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0dc3-104">SYNTAX</span></span>

### <span data-ttu-id="b0dc3-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b0dc3-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dc3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dc3-106">ByResourceId</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dc3-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b0dc3-107">ByIntegrationRuntimeObject</span></span>
```
New-AzureRmDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0dc3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0dc3-108">DESCRIPTION</span></span>
<span data-ttu-id="b0dc3-109">A **New-AzureRmDataFactoryV2IntegrationRuntimeKey** parancsmag az integrációs futtatókörnyezetet az "kulcsnév" paraméter által megadott kulccsal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-109">The cmdlet **New-AzureRmDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="b0dc3-110">Az előző kulcs érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="b0dc3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b0dc3-111">EXAMPLES</span></span>

### <span data-ttu-id="b0dc3-112">1. példa: új kulcs létrehozása integrációs futtatókörnyezethez</span><span class="sxs-lookup"><span data-stu-id="b0dc3-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="b0dc3-113">A parancsmag újragenerálja a "authKey2" "selfhost-IR" nevű integrációs futásidejű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b0dc3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0dc3-114">PARAMETERS</span></span>

### <span data-ttu-id="b0dc3-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b0dc3-115">-DataFactoryName</span></span>
<span data-ttu-id="b0dc3-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-116">The data factory name.</span></span>

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

### <span data-ttu-id="b0dc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dc3-117">-DefaultProfile</span></span>
<span data-ttu-id="b0dc3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0dc3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b0dc3-119">-Force</span></span>
<span data-ttu-id="b0dc3-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b0dc3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0dc3-121">-InputObject</span></span>
<span data-ttu-id="b0dc3-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="b0dc3-123">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="b0dc3-123">-KeyName</span></span>
<span data-ttu-id="b0dc3-124">Az önkiszolgáló integrációs futtatókörnyezet hitelesítő kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dc3-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b0dc3-125">-Name</span></span>
<span data-ttu-id="b0dc3-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-126">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dc3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0dc3-127">-ResourceGroupName</span></span>
<span data-ttu-id="b0dc3-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-128">The resource group name.</span></span>

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

### <span data-ttu-id="b0dc3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dc3-129">-ResourceId</span></span>
<span data-ttu-id="b0dc3-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b0dc3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b0dc3-131">-Confirm</span></span>
<span data-ttu-id="b0dc3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0dc3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0dc3-133">-WhatIf</span></span>
<span data-ttu-id="b0dc3-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b0dc3-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b0dc3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dc3-135">CommonParameters</span></span>
<span data-ttu-id="b0dc3-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0dc3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dc3-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0dc3-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dc3-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0dc3-138">INPUTS</span></span>

### <span data-ttu-id="b0dc3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b0dc3-139">System.String</span></span>
<span data-ttu-id="b0dc3-140">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b0dc3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b0dc3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0dc3-141">OUTPUTS</span></span>

### <span data-ttu-id="b0dc3-142">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="b0dc3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="b0dc3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0dc3-143">NOTES</span></span>

## <span data-ttu-id="b0dc3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0dc3-144">RELATED LINKS</span></span>

[<span data-ttu-id="b0dc3-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="b0dc3-145">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
