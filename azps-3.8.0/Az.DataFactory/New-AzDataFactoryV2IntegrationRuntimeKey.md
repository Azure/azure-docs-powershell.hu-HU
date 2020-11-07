---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847201"
---
# <span data-ttu-id="55eac-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="55eac-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="55eac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55eac-102">SYNOPSIS</span></span>
<span data-ttu-id="55eac-103">Önkiszolgáló integrációs futásidejű kulcs újbóli létrehozása</span><span class="sxs-lookup"><span data-stu-id="55eac-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="55eac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55eac-104">SYNTAX</span></span>

### <span data-ttu-id="55eac-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="55eac-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55eac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="55eac-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55eac-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="55eac-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55eac-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="55eac-108">DESCRIPTION</span></span>
<span data-ttu-id="55eac-109">A **New-AzDataFactoryV2IntegrationRuntimeKey** parancsmag az integrációs futtatókörnyezetet az "kulcsnév" paraméter által megadott kulccsal hozza létre.</span><span class="sxs-lookup"><span data-stu-id="55eac-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="55eac-110">Az előző kulcs érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="55eac-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="55eac-111">Példák</span><span class="sxs-lookup"><span data-stu-id="55eac-111">EXAMPLES</span></span>

### <span data-ttu-id="55eac-112">1. példa: új kulcs létrehozása integrációs futtatókörnyezethez</span><span class="sxs-lookup"><span data-stu-id="55eac-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="55eac-113">A parancsmag újragenerálja a "authKey2" "selfhost-IR" nevű integrációs futásidejű kulcsot.</span><span class="sxs-lookup"><span data-stu-id="55eac-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="55eac-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55eac-114">PARAMETERS</span></span>

### <span data-ttu-id="55eac-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="55eac-115">-DataFactoryName</span></span>
<span data-ttu-id="55eac-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="55eac-116">The data factory name.</span></span>

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

### <span data-ttu-id="55eac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55eac-117">-DefaultProfile</span></span>
<span data-ttu-id="55eac-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="55eac-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55eac-119">-Force</span><span class="sxs-lookup"><span data-stu-id="55eac-119">-Force</span></span>
<span data-ttu-id="55eac-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="55eac-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="55eac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55eac-121">-InputObject</span></span>
<span data-ttu-id="55eac-122">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="55eac-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="55eac-123">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="55eac-123">-KeyName</span></span>
<span data-ttu-id="55eac-124">Az önkiszolgáló integrációs futtatókörnyezet hitelesítő kulcsának neve.</span><span class="sxs-lookup"><span data-stu-id="55eac-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="55eac-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="55eac-125">-Name</span></span>
<span data-ttu-id="55eac-126">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="55eac-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="55eac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55eac-127">-ResourceGroupName</span></span>
<span data-ttu-id="55eac-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="55eac-128">The resource group name.</span></span>

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

### <span data-ttu-id="55eac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55eac-129">-ResourceId</span></span>
<span data-ttu-id="55eac-130">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="55eac-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="55eac-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="55eac-131">-Confirm</span></span>
<span data-ttu-id="55eac-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="55eac-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55eac-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55eac-133">-WhatIf</span></span>
<span data-ttu-id="55eac-134">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="55eac-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="55eac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55eac-135">CommonParameters</span></span>
<span data-ttu-id="55eac-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55eac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55eac-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55eac-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55eac-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55eac-138">INPUTS</span></span>

### <span data-ttu-id="55eac-139">System. String</span><span class="sxs-lookup"><span data-stu-id="55eac-139">System.String</span></span>

### <span data-ttu-id="55eac-140">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="55eac-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="55eac-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55eac-141">OUTPUTS</span></span>

### <span data-ttu-id="55eac-142">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="55eac-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="55eac-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55eac-143">NOTES</span></span>

## <span data-ttu-id="55eac-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55eac-144">RELATED LINKS</span></span>

[<span data-ttu-id="55eac-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="55eac-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
