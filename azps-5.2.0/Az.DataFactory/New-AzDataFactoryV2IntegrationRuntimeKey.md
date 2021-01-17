---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 07cb597f5ca3793e3eb8db3fe153fafaa94f3501
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324488"
---
# <span data-ttu-id="44f94-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="44f94-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="44f94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44f94-102">SYNOPSIS</span></span>
<span data-ttu-id="44f94-103">Az önkiszolgáló integráció futásidejű kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="44f94-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="44f94-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44f94-104">SYNTAX</span></span>

### <span data-ttu-id="44f94-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="44f94-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44f94-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="44f94-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44f94-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="44f94-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44f94-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44f94-108">DESCRIPTION</span></span>
<span data-ttu-id="44f94-109">A **New-AzDataFactoryV2IntegrationRuntimeKey** parancsmag a "KeyName" paraméterben megadott kulcsnévvel újragenerálja az integrációs futási kulcsot.</span><span class="sxs-lookup"><span data-stu-id="44f94-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="44f94-110">Az előző kulcs érvénytelen.</span><span class="sxs-lookup"><span data-stu-id="44f94-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="44f94-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44f94-111">EXAMPLES</span></span>

### <span data-ttu-id="44f94-112">1. példa: Új kulcs létrehozása integrációs futásidejű futási időben</span><span class="sxs-lookup"><span data-stu-id="44f94-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="44f94-113">A parancsmag a "test-selfhost-ir" nevű integrációs runtime-hoz újragenerálja az "authKey2" kulcsot.</span><span class="sxs-lookup"><span data-stu-id="44f94-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="44f94-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44f94-114">PARAMETERS</span></span>

### <span data-ttu-id="44f94-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="44f94-115">-DataFactoryName</span></span>
<span data-ttu-id="44f94-116">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="44f94-116">The data factory name.</span></span>

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

### <span data-ttu-id="44f94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44f94-117">-DefaultProfile</span></span>
<span data-ttu-id="44f94-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44f94-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44f94-119">-Force</span><span class="sxs-lookup"><span data-stu-id="44f94-119">-Force</span></span>
<span data-ttu-id="44f94-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="44f94-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="44f94-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44f94-121">-InputObject</span></span>
<span data-ttu-id="44f94-122">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="44f94-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="44f94-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="44f94-123">-KeyName</span></span>
<span data-ttu-id="44f94-124">Az önkiszolgáló integrációs futásidejű hitelesítési kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="44f94-124">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="44f94-125">-Name</span><span class="sxs-lookup"><span data-stu-id="44f94-125">-Name</span></span>
<span data-ttu-id="44f94-126">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="44f94-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="44f94-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44f94-127">-ResourceGroupName</span></span>
<span data-ttu-id="44f94-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44f94-128">The resource group name.</span></span>

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

### <span data-ttu-id="44f94-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44f94-129">-ResourceId</span></span>
<span data-ttu-id="44f94-130">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="44f94-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="44f94-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44f94-131">-Confirm</span></span>
<span data-ttu-id="44f94-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44f94-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44f94-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44f94-133">-WhatIf</span></span>
<span data-ttu-id="44f94-134">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="44f94-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="44f94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44f94-135">CommonParameters</span></span>
<span data-ttu-id="44f94-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44f94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44f94-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44f94-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44f94-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44f94-138">INPUTS</span></span>

### <span data-ttu-id="44f94-139">System.String</span><span class="sxs-lookup"><span data-stu-id="44f94-139">System.String</span></span>

### <span data-ttu-id="44f94-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="44f94-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="44f94-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44f94-141">OUTPUTS</span></span>

### <span data-ttu-id="44f94-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="44f94-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="44f94-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44f94-143">NOTES</span></span>

## <span data-ttu-id="44f94-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44f94-144">RELATED LINKS</span></span>

[<span data-ttu-id="44f94-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="44f94-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
