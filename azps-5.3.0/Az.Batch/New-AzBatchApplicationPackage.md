---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478281"
---
# <span data-ttu-id="3e8a0-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e8a0-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="3e8a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="3e8a0-103">Alkalmazáscsomagot hoz létre egy Batch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="3e8a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-104">SYNTAX</span></span>

### <span data-ttu-id="3e8a0-105">UploadAndActivate (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e8a0-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e8a0-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3e8a0-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e8a0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-107">DESCRIPTION</span></span>
<span data-ttu-id="3e8a0-108">A **New-AzBatchApplicationPackage** parancsmag létrehoz egy alkalmazáscsomagot egy Azure Batch-fiókban.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="3e8a0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e8a0-109">EXAMPLES</span></span>

### <span data-ttu-id="3e8a0-110">1. példa: Alkalmazáscsomag telepítése Kötegfiókba</span><span class="sxs-lookup"><span data-stu-id="3e8a0-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="3e8a0-111">Ez a parancs létrehozza és aktiválja a Litware alkalmazás 1.0-s verzióját, és feltölti a litware.1.0.zip tartalmát az alkalmazáscsomag tartalmaként.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="3e8a0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-112">PARAMETERS</span></span>

### <span data-ttu-id="3e8a0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e8a0-113">-AccountName</span></span>
<span data-ttu-id="3e8a0-114">Annak a Batch-fióknak a neve, amelyhez ez a parancsmag hozzáad egy alkalmazáscsomagot.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="3e8a0-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="3e8a0-115">-ActivateOnly</span></span>
<span data-ttu-id="3e8a0-116">Azt jelzi, hogy ez a parancsmag egy már feltöltött alkalmazáscsomagot aktivál.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="3e8a0-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="3e8a0-117">-ApplicationName</span></span>
<span data-ttu-id="3e8a0-118">Az alkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e8a0-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="3e8a0-119">-ApplicationVersion</span></span>
<span data-ttu-id="3e8a0-120">Az alkalmazás verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="3e8a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e8a0-121">-DefaultProfile</span></span>
<span data-ttu-id="3e8a0-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e8a0-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="3e8a0-123">-FilePath</span></span>
<span data-ttu-id="3e8a0-124">Az alkalmazáscsomag bináris fájljaként feltöltni kívánt fájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="3e8a0-125">-Format</span><span class="sxs-lookup"><span data-stu-id="3e8a0-125">-Format</span></span>
<span data-ttu-id="3e8a0-126">Az alkalmazáscsomag bináris fájlformátumát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="3e8a0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e8a0-127">-ResourceGroupName</span></span>
<span data-ttu-id="3e8a0-128">A Batch-fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="3e8a0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e8a0-129">CommonParameters</span></span>
<span data-ttu-id="3e8a0-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e8a0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e8a0-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e8a0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e8a0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e8a0-132">INPUTS</span></span>

### <span data-ttu-id="3e8a0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3e8a0-133">System.String</span></span>

### <span data-ttu-id="3e8a0-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e8a0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e8a0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e8a0-135">OUTPUTS</span></span>

### <span data-ttu-id="3e8a0-136">Microsoft.Azure.Commands.Bat. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e8a0-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="3e8a0-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e8a0-137">NOTES</span></span>

## <span data-ttu-id="3e8a0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e8a0-138">RELATED LINKS</span></span>

[<span data-ttu-id="3e8a0-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e8a0-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="3e8a0-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e8a0-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="3e8a0-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e8a0-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="3e8a0-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e8a0-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="3e8a0-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="3e8a0-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="3e8a0-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="3e8a0-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


