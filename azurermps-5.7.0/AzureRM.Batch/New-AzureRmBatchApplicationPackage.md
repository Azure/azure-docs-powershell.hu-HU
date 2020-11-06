---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 621aa03b2819815dc538650ea30120c63009235e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503095"
---
# <span data-ttu-id="3036a-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3036a-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="3036a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3036a-102">SYNOPSIS</span></span>
<span data-ttu-id="3036a-103">Alkalmazásspecifikus csomagot hoz létre egy köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="3036a-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3036a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3036a-104">SYNTAX</span></span>

### <span data-ttu-id="3036a-105">UploadAndActivate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3036a-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3036a-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3036a-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3036a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3036a-107">DESCRIPTION</span></span>
<span data-ttu-id="3036a-108">A **New-AzureRmBatchApplicationPackage** parancsmag az Azure batch-fiókokban létrehoz egy alkalmazáscsomag.</span><span class="sxs-lookup"><span data-stu-id="3036a-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="3036a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3036a-109">EXAMPLES</span></span>

### <span data-ttu-id="3036a-110">1. példa: alkalmazáscsomag telepítése kötegelt fiókba</span><span class="sxs-lookup"><span data-stu-id="3036a-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="3036a-111">Ez a parancs létrehozza és aktiválja a Bárdos Iparcikk alkalmazás 1,0 verzióját, és feltölti a litware.1.0.zip tartalmát az alkalmazáscsomag tartalmaként.</span><span class="sxs-lookup"><span data-stu-id="3036a-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="3036a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3036a-112">PARAMETERS</span></span>

### <span data-ttu-id="3036a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3036a-113">-AccountName</span></span>
<span data-ttu-id="3036a-114">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag hozzáad egy alkalmazáscsomag használatát.</span><span class="sxs-lookup"><span data-stu-id="3036a-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3036a-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3036a-115">-ActivateOnly</span></span>
<span data-ttu-id="3036a-116">Jelzi, hogy ez a parancsmag egy már feltöltött alkalmazáscsomag aktiválása.</span><span class="sxs-lookup"><span data-stu-id="3036a-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3036a-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3036a-117">-ApplicationId</span></span>
<span data-ttu-id="3036a-118">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3036a-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="3036a-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3036a-119">-ApplicationVersion</span></span>
<span data-ttu-id="3036a-120">Az alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3036a-120">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3036a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3036a-121">-DefaultProfile</span></span>
<span data-ttu-id="3036a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3036a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3036a-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3036a-123">-FilePath</span></span>
<span data-ttu-id="3036a-124">Annak a fájlnak a megadása, amelyet az alkalmazáscsomag bináris fájlként kell feltölteni.</span><span class="sxs-lookup"><span data-stu-id="3036a-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3036a-125">Formátumú</span><span class="sxs-lookup"><span data-stu-id="3036a-125">-Format</span></span>
<span data-ttu-id="3036a-126">Az alkalmazáscsomag bináris fájljának formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3036a-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3036a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3036a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3036a-128">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3036a-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3036a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3036a-129">CommonParameters</span></span>
<span data-ttu-id="3036a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3036a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3036a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3036a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3036a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3036a-132">INPUTS</span></span>

### <span data-ttu-id="3036a-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="3036a-133">None</span></span>
<span data-ttu-id="3036a-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3036a-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3036a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3036a-135">OUTPUTS</span></span>

### <span data-ttu-id="3036a-136">Microsoft.Azure.Commands.BatCH. Modellek. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3036a-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="3036a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3036a-137">NOTES</span></span>

## <span data-ttu-id="3036a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3036a-138">RELATED LINKS</span></span>

[<span data-ttu-id="3036a-139">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3036a-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="3036a-140">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3036a-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3036a-141">Új – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3036a-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="3036a-142">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3036a-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="3036a-143">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3036a-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="3036a-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3036a-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


