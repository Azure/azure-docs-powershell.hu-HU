---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491966"
---
# <span data-ttu-id="9bd92-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="9bd92-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="9bd92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9bd92-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd92-103">Hitelesítő adatok titkosítása a kapcsolódó szolgáltatásban meghatározott integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="9bd92-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bd92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9bd92-104">SYNTAX</span></span>

### <span data-ttu-id="9bd92-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9bd92-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bd92-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9bd92-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9bd92-107">DESCRIPTION</span></span>
<span data-ttu-id="9bd92-108">A New-AzureRmDataFactoryV2LinkedServiceEncryptCredential parancsmag hitelesítő adatait titkosítja a kapcsolt szolgáltatásban a megadott integrációs futtatókörnyezetkel.</span><span class="sxs-lookup"><span data-stu-id="9bd92-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="9bd92-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9bd92-109">EXAMPLES</span></span>

### <span data-ttu-id="9bd92-110">1. példa: creadentials titkosítása egy kapcsolt szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="9bd92-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="9bd92-111">Ez a parancs titkosítja a hitelesítő adatokat a fájl D:\sql.jsa myIR nevű integrációs futtatókörnyezettel.</span><span class="sxs-lookup"><span data-stu-id="9bd92-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="9bd92-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9bd92-112">PARAMETERS</span></span>

### <span data-ttu-id="9bd92-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9bd92-113">-DataFactory</span></span>
<span data-ttu-id="9bd92-114">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="9bd92-114">The data factory object.</span></span>

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

### <span data-ttu-id="9bd92-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9bd92-115">-DataFactoryName</span></span>
<span data-ttu-id="9bd92-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="9bd92-116">The data factory name.</span></span>

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

### <span data-ttu-id="9bd92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd92-117">-DefaultProfile</span></span>
<span data-ttu-id="9bd92-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9bd92-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bd92-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9bd92-119">-DefinitionFile</span></span>
<span data-ttu-id="9bd92-120">A JSON-fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="9bd92-120">The JSON file path.</span></span>

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

### <span data-ttu-id="9bd92-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9bd92-121">-Force</span></span>
<span data-ttu-id="9bd92-122">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="9bd92-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9bd92-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9bd92-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9bd92-124">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="9bd92-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="9bd92-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd92-125">-ResourceGroupName</span></span>
<span data-ttu-id="9bd92-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="9bd92-126">The resource group name.</span></span>

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

### <span data-ttu-id="9bd92-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9bd92-127">-Confirm</span></span>
<span data-ttu-id="9bd92-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9bd92-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd92-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd92-129">-WhatIf</span></span>
<span data-ttu-id="9bd92-130">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9bd92-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9bd92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd92-131">CommonParameters</span></span>
<span data-ttu-id="9bd92-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9bd92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd92-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bd92-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd92-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd92-134">INPUTS</span></span>

### <span data-ttu-id="9bd92-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd92-135">System.String</span></span>

### <span data-ttu-id="9bd92-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9bd92-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9bd92-137">Paraméterek: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bd92-137">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="9bd92-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9bd92-138">OUTPUTS</span></span>

### <span data-ttu-id="9bd92-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9bd92-139">System.String</span></span>

## <span data-ttu-id="9bd92-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9bd92-140">NOTES</span></span>

## <span data-ttu-id="9bd92-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9bd92-141">RELATED LINKS</span></span>
