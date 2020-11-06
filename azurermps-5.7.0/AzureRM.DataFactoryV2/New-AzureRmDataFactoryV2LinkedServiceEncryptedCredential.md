---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 47121a8a06e2b4aa4e48218d1be4694743c00de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492310"
---
# <span data-ttu-id="4aaef-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="4aaef-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="4aaef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4aaef-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaef-103">Hitelesítő adatok titkosítása a kapcsolódó szolgáltatásban meghatározott integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="4aaef-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aaef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4aaef-104">SYNTAX</span></span>

### <span data-ttu-id="4aaef-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4aaef-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aaef-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4aaef-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aaef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4aaef-107">DESCRIPTION</span></span>
<span data-ttu-id="4aaef-108">A New-AzureRmDataFactoryV2LinkedServiceEncryptCredential parancsmag hitelesítő adatait titkosítja a kapcsolt szolgáltatásban a megadott integrációs futtatókörnyezetkel.</span><span class="sxs-lookup"><span data-stu-id="4aaef-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="4aaef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4aaef-109">EXAMPLES</span></span>

### <span data-ttu-id="4aaef-110">1. példa: creadentials titkosítása egy kapcsolt szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="4aaef-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="4aaef-111">Ez a parancs titkosítja a hitelesítő adatokat a fájl D:\sql.jsa myIR nevű integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="4aaef-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="4aaef-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4aaef-112">PARAMETERS</span></span>

### <span data-ttu-id="4aaef-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4aaef-113">-DataFactory</span></span>
<span data-ttu-id="4aaef-114">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="4aaef-114">The data factory object.</span></span>

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

### <span data-ttu-id="4aaef-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4aaef-115">-DataFactoryName</span></span>
<span data-ttu-id="4aaef-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="4aaef-116">The data factory name.</span></span>

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

### <span data-ttu-id="4aaef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aaef-117">-DefaultProfile</span></span>
<span data-ttu-id="4aaef-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4aaef-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aaef-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4aaef-119">-DefinitionFile</span></span>
<span data-ttu-id="4aaef-120">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="4aaef-120">The JSON file path.</span></span>

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

### <span data-ttu-id="4aaef-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4aaef-121">-Force</span></span>
<span data-ttu-id="4aaef-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="4aaef-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4aaef-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4aaef-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="4aaef-124">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="4aaef-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="4aaef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aaef-125">-ResourceGroupName</span></span>
<span data-ttu-id="4aaef-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4aaef-126">The resource group name.</span></span>

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

### <span data-ttu-id="4aaef-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4aaef-127">-Confirm</span></span>
<span data-ttu-id="4aaef-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4aaef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aaef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaef-129">-WhatIf</span></span>
<span data-ttu-id="4aaef-130">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4aaef-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4aaef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaef-131">CommonParameters</span></span>
<span data-ttu-id="4aaef-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4aaef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaef-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aaef-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaef-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aaef-134">INPUTS</span></span>

### <span data-ttu-id="4aaef-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4aaef-135">System.String</span></span>
<span data-ttu-id="4aaef-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4aaef-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4aaef-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aaef-137">OUTPUTS</span></span>

### <span data-ttu-id="4aaef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4aaef-138">System.String</span></span>

## <span data-ttu-id="4aaef-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4aaef-139">NOTES</span></span>

## <span data-ttu-id="4aaef-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aaef-140">RELATED LINKS</span></span>

