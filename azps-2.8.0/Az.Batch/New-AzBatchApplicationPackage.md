---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 0e5494506873917be7897c547eca900174f5bcab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667694"
---
# <span data-ttu-id="3a3b9-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a3b9-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="3a3b9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a3b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3b9-103">Alkalmazásspecifikus csomagot hoz létre egy köteg fiókban.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="3a3b9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a3b9-104">SYNTAX</span></span>

### <span data-ttu-id="3a3b9-105">UploadAndActivate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3a3b9-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a3b9-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3a3b9-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a3b9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a3b9-107">DESCRIPTION</span></span>
<span data-ttu-id="3a3b9-108">A **New-AzBatchApplicationPackage** parancsmag az Azure batch-fiókokban létrehoz egy alkalmazáscsomag.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="3a3b9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3a3b9-109">EXAMPLES</span></span>

### <span data-ttu-id="3a3b9-110">1. példa: alkalmazáscsomag telepítése kötegelt fiókba</span><span class="sxs-lookup"><span data-stu-id="3a3b9-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="3a3b9-111">Ez a parancs létrehozza és aktiválja a Bárdos Iparcikk alkalmazás 1,0 verzióját, és feltölti a litware.1.0.zip tartalmát az alkalmazáscsomag tartalmaként.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="3a3b9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a3b9-112">PARAMETERS</span></span>

### <span data-ttu-id="3a3b9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a3b9-113">-AccountName</span></span>
<span data-ttu-id="3a3b9-114">Annak a kötegelt fióknak a nevét adja meg, amelyre a parancsmag hozzáad egy alkalmazáscsomag használatát.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3b9-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3a3b9-115">-ActivateOnly</span></span>
<span data-ttu-id="3a3b9-116">Jelzi, hogy ez a parancsmag egy már feltöltött alkalmazáscsomag aktiválása.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3b9-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3a3b9-117">-ApplicationId</span></span>
<span data-ttu-id="3a3b9-118">Az alkalmazás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="3a3b9-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3a3b9-119">-ApplicationVersion</span></span>
<span data-ttu-id="3a3b9-120">Az alkalmazás verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3b9-121">-DefaultProfile</span></span>
<span data-ttu-id="3a3b9-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a3b9-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3a3b9-123">-FilePath</span></span>
<span data-ttu-id="3a3b9-124">Annak a fájlnak a megadása, amelyet az alkalmazáscsomag bináris fájlként kell feltölteni.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3b9-125">Formátumú</span><span class="sxs-lookup"><span data-stu-id="3a3b9-125">-Format</span></span>
<span data-ttu-id="3a3b9-126">Az alkalmazáscsomag bináris fájljának formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a3b9-128">A köteg fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a3b9-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3b9-129">CommonParameters</span></span>
<span data-ttu-id="3a3b9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a3b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3b9-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a3b9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3b9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a3b9-132">INPUTS</span></span>

### <span data-ttu-id="3a3b9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a3b9-133">System.String</span></span>

### <span data-ttu-id="3a3b9-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a3b9-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3a3b9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a3b9-135">OUTPUTS</span></span>

### <span data-ttu-id="3a3b9-136">Microsoft.Azure.Commands.BatCH. Modellek. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a3b9-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="3a3b9-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a3b9-137">NOTES</span></span>

## <span data-ttu-id="3a3b9-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a3b9-138">RELATED LINKS</span></span>

[<span data-ttu-id="3a3b9-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a3b9-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="3a3b9-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a3b9-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="3a3b9-141">Új – AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a3b9-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="3a3b9-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a3b9-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="3a3b9-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3a3b9-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="3a3b9-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3a3b9-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


