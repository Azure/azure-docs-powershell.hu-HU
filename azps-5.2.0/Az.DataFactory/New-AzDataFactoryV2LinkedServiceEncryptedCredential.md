---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344634"
---
# <span data-ttu-id="9b98f-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="9b98f-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="9b98f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b98f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b98f-103">Hitelesítő adatok titkosítása a csatolt szolgáltatásban megadott integrációs futásidejű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9b98f-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="9b98f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b98f-104">SYNTAX</span></span>

### <span data-ttu-id="9b98f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b98f-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b98f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9b98f-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b98f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b98f-107">DESCRIPTION</span></span>
<span data-ttu-id="9b98f-108">A New-AzDataFactoryV2LinkedServiceEncryptedCredential hitelesítő adatok titkosítása a csatolt szolgáltatásban megadott integrációs futásidejű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="9b98f-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="9b98f-109">Győződjön meg arról, hogy az alábbi előfeltételek teljesülnek:</span><span class="sxs-lookup"><span data-stu-id="9b98f-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="9b98f-110">**A távoli elérés** engedélyezve van az önkiszolgáló integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="9b98f-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="9b98f-111">A parancsmag végrehajtásához a Powershell 7.0-s vagy újabb parancsmag használható.</span><span class="sxs-lookup"><span data-stu-id="9b98f-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="9b98f-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b98f-112">EXAMPLES</span></span>

### <span data-ttu-id="9b98f-113">1. példa: Hitelesítő adatok titkosítása csatolt szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="9b98f-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="9b98f-114">Ez a parancs titkosítja a hitelesítő C:\samples\WikiSample\TaxiDemo1.jsa test-selfhost-ir nevű integrációs futásidejű fájlban.</span><span class="sxs-lookup"><span data-stu-id="9b98f-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="9b98f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b98f-115">PARAMETERS</span></span>

### <span data-ttu-id="9b98f-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b98f-116">-DataFactory</span></span>
<span data-ttu-id="9b98f-117">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="9b98f-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b98f-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9b98f-118">-DataFactoryName</span></span>
<span data-ttu-id="9b98f-119">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="9b98f-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b98f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b98f-120">-DefaultProfile</span></span>
<span data-ttu-id="9b98f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b98f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b98f-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9b98f-122">-DefinitionFile</span></span>
<span data-ttu-id="9b98f-123">A JSON fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9b98f-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b98f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9b98f-124">-Force</span></span>
<span data-ttu-id="9b98f-125">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="9b98f-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9b98f-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9b98f-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9b98f-127">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="9b98f-127">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b98f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b98f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b98f-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9b98f-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b98f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b98f-130">-Confirm</span></span>
<span data-ttu-id="9b98f-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9b98f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b98f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b98f-132">-WhatIf</span></span>
<span data-ttu-id="9b98f-133">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9b98f-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9b98f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b98f-134">CommonParameters</span></span>
<span data-ttu-id="9b98f-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b98f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b98f-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b98f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b98f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b98f-137">INPUTS</span></span>

### <span data-ttu-id="9b98f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9b98f-138">System.String</span></span>

### <span data-ttu-id="9b98f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9b98f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="9b98f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b98f-140">OUTPUTS</span></span>

### <span data-ttu-id="9b98f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9b98f-141">System.String</span></span>

## <span data-ttu-id="9b98f-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b98f-142">NOTES</span></span>

## <span data-ttu-id="9b98f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b98f-143">RELATED LINKS</span></span>
