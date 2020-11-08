---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183799"
---
# <span data-ttu-id="11e5a-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="11e5a-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="11e5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="11e5a-103">BLOB-tartománnyal létrehozott objektumot hoz létre a tárolási fiók visszaállításához.</span><span class="sxs-lookup"><span data-stu-id="11e5a-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="11e5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11e5a-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11e5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="11e5a-106">A **New-AzStorageBlobRangeToRestore** parancsmag létrehoz egy blob-alapú objektumot, amelyet a Restore-AzStorageBlobRange használhat.</span><span class="sxs-lookup"><span data-stu-id="11e5a-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="11e5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11e5a-107">EXAMPLES</span></span>

### <span data-ttu-id="11e5a-108">Példa 1: a visszaállítandó blob-tartományok létrehozása</span><span class="sxs-lookup"><span data-stu-id="11e5a-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="11e5a-109">Ez a parancs a container1/blob1 (include) kezdetű blob-tartománnyal hoz létre, és a container2/blob2 (kizár) végződést adja vissza.</span><span class="sxs-lookup"><span data-stu-id="11e5a-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="11e5a-110">2. példa: a blob-intervallumot hozza létre, amely az első blobtól a betűrendes sorrendtől az adott blobba kerül (kihagyva).</span><span class="sxs-lookup"><span data-stu-id="11e5a-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="11e5a-111">Ez a parancs létrehoz egy blob-intervallumot, amely a betűrendes sorrendtől az első blobtól egy adott blob container2/blob2 (kizár) fog visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="11e5a-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="11e5a-112">3. példa: egy blob-intervallumot hoz létre, amely egy adott blobból (belefoglalt), betűrendben az utolsó blobba fog visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="11e5a-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="11e5a-113">Ez a parancs létrehoz egy blob-cellatartományt, amely egy adott blob-container1/blob1 (include), betűrendben az utolsó blobba fog visszaállítani.</span><span class="sxs-lookup"><span data-stu-id="11e5a-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="11e5a-114">4. példa: blob-tartománnyal hoz létre minden blobot.</span><span class="sxs-lookup"><span data-stu-id="11e5a-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="11e5a-115">Ez a parancs létrehoz egy blob-cellatartományt, amely az összes blobot visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="11e5a-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="11e5a-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11e5a-116">PARAMETERS</span></span>

### <span data-ttu-id="11e5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e5a-117">-DefaultProfile</span></span>
<span data-ttu-id="11e5a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11e5a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e5a-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="11e5a-119">-EndRange</span></span>
<span data-ttu-id="11e5a-120">Adja meg a blob-visszaállítási végpontot.</span><span class="sxs-lookup"><span data-stu-id="11e5a-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="11e5a-121">A végződési tartományok kimaradnak a visszaállítási Blobs bővítményben.</span><span class="sxs-lookup"><span data-stu-id="11e5a-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="11e5a-122">Állítsa üres strng a végére való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="11e5a-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e5a-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="11e5a-123">-StartRange</span></span>
<span data-ttu-id="11e5a-124">Adja meg a blob-helyreállítási indítási tartománnyal.</span><span class="sxs-lookup"><span data-stu-id="11e5a-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="11e5a-125">A Start-tartományok szerepelni fognak a visszaállítási festékfoltok között.</span><span class="sxs-lookup"><span data-stu-id="11e5a-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="11e5a-126">Állítsa azt üres karakterláncként az elejétől való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="11e5a-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e5a-127">CommonParameters</span></span>
<span data-ttu-id="11e5a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11e5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e5a-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e5a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e5a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11e5a-130">INPUTS</span></span>

### <span data-ttu-id="11e5a-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="11e5a-131">None</span></span>

## <span data-ttu-id="11e5a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11e5a-132">OUTPUTS</span></span>

### <span data-ttu-id="11e5a-133">Microsoft. Azure. Command. Management. Storage. models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="11e5a-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="11e5a-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11e5a-134">NOTES</span></span>

## <span data-ttu-id="11e5a-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11e5a-135">RELATED LINKS</span></span>
