---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 8571e210a39bc1d617b391eb4cf71aa45a34d69c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667019"
---
# <span data-ttu-id="f9ab7-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f9ab7-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="f9ab7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ab7-103">Önkiszolgáló integrációs futásidejű kulcs újbóli létrehozása</span><span class="sxs-lookup"><span data-stu-id="f9ab7-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="f9ab7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9ab7-104">SYNTAX</span></span>

### <span data-ttu-id="f9ab7-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f9ab7-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ab7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ab7-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9ab7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f9ab7-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ab7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9ab7-108">DESCRIPTION</span></span>
<span data-ttu-id="f9ab7-109">A **New-AzDataFactoryV2IntegrationRuntimeKey** parancsmag az integrációs futtatókörnyezetet az "kulcsnév" paraméter által megadott kulccsal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="f9ab7-110">Az előző kulcs érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="f9ab7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f9ab7-111">EXAMPLES</span></span>

### <span data-ttu-id="f9ab7-112">1. példa: új kulcs létrehozása integrációs futtatókörnyezethez</span><span class="sxs-lookup"><span data-stu-id="f9ab7-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="f9ab7-113">A parancsmag újragenerálja a "authKey2" "selfhost-IR" nevű integrációs futásidejű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f9ab7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9ab7-114">PARAMETERS</span></span>

### <span data-ttu-id="f9ab7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f9ab7-115">-DataFactoryName</span></span>
<span data-ttu-id="f9ab7-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-116">The data factory name.</span></span>

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

### <span data-ttu-id="f9ab7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ab7-117">-DefaultProfile</span></span>
<span data-ttu-id="f9ab7-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9ab7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f9ab7-119">-Force</span></span>
<span data-ttu-id="f9ab7-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f9ab7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9ab7-121">-InputObject</span></span>
<span data-ttu-id="f9ab7-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="f9ab7-123">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="f9ab7-123">-KeyName</span></span>
<span data-ttu-id="f9ab7-124">Az önkiszolgáló integrációs futtatókörnyezet hitelesítő kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ab7-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f9ab7-125">-Name</span></span>
<span data-ttu-id="f9ab7-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9ab7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9ab7-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9ab7-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-128">The resource group name.</span></span>

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

### <span data-ttu-id="f9ab7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9ab7-129">-ResourceId</span></span>
<span data-ttu-id="f9ab7-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f9ab7-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f9ab7-131">-Confirm</span></span>
<span data-ttu-id="f9ab7-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9ab7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ab7-133">-WhatIf</span></span>
<span data-ttu-id="f9ab7-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f9ab7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ab7-135">CommonParameters</span></span>
<span data-ttu-id="f9ab7-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9ab7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ab7-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ab7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ab7-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9ab7-138">INPUTS</span></span>

### <span data-ttu-id="f9ab7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f9ab7-139">System.String</span></span>

### <span data-ttu-id="f9ab7-140">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f9ab7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f9ab7-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9ab7-141">OUTPUTS</span></span>

### <span data-ttu-id="f9ab7-142">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="f9ab7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="f9ab7-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9ab7-143">NOTES</span></span>

## <span data-ttu-id="f9ab7-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9ab7-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9ab7-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f9ab7-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
