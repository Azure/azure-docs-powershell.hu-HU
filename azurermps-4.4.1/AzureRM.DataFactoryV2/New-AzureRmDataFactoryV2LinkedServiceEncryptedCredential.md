---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 9960a34d19c4016461ddfc53a37f83d3e73e7526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679782"
---
# <span data-ttu-id="278fa-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="278fa-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="278fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="278fa-102">SYNOPSIS</span></span>
<span data-ttu-id="278fa-103">Hitelesítő adatok titkosítása a kapcsolódó szolgáltatásban meghatározott integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="278fa-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="278fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="278fa-104">SYNTAX</span></span>

### <span data-ttu-id="278fa-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="278fa-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="278fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="278fa-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="278fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="278fa-107">DESCRIPTION</span></span>
<span data-ttu-id="278fa-108">A New-AzureRmDataFactoryV2LinkedServiceEncryptCredential parancsmag hitelesítő adatait titkosítja a kapcsolt szolgáltatásban a megadott integrációs futtatókörnyezetkel.</span><span class="sxs-lookup"><span data-stu-id="278fa-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="278fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="278fa-109">EXAMPLES</span></span>

### <span data-ttu-id="278fa-110">1. példa: creadentials titkosítása egy kapcsolt szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="278fa-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="278fa-111">Ez a parancs titkosítja a hitelesítő adatokat a fájl D:\sql.jsa myIR nevű integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="278fa-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="278fa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="278fa-112">PARAMETERS</span></span>

### <span data-ttu-id="278fa-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="278fa-113">-DataFactory</span></span>
<span data-ttu-id="278fa-114">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="278fa-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="278fa-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="278fa-115">-DataFactoryName</span></span>
<span data-ttu-id="278fa-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="278fa-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278fa-117">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="278fa-117">-DefinitionFile</span></span>
<span data-ttu-id="278fa-118">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="278fa-118">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278fa-119">-Force</span><span class="sxs-lookup"><span data-stu-id="278fa-119">-Force</span></span>
<span data-ttu-id="278fa-120">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="278fa-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="278fa-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="278fa-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="278fa-122">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="278fa-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="278fa-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="278fa-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="278fa-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="278fa-125">-Confirm</span></span>
<span data-ttu-id="278fa-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="278fa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278fa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278fa-127">-WhatIf</span></span>
<span data-ttu-id="278fa-128">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="278fa-128">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="278fa-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="278fa-129">INPUTS</span></span>

### <span data-ttu-id="278fa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="278fa-130">System.String</span></span>
<span data-ttu-id="278fa-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="278fa-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="278fa-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="278fa-132">OUTPUTS</span></span>

### <span data-ttu-id="278fa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="278fa-133">System.String</span></span>


## <span data-ttu-id="278fa-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="278fa-134">NOTES</span></span>

## <span data-ttu-id="278fa-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="278fa-135">RELATED LINKS</span></span>

