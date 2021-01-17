---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324809"
---
# <span data-ttu-id="1a069-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="1a069-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="1a069-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a069-102">SYNOPSIS</span></span>
<span data-ttu-id="1a069-103">Blobtartomány-objektumot hoz létre a tárfiók visszaállításához.</span><span class="sxs-lookup"><span data-stu-id="1a069-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="1a069-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1a069-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a069-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1a069-105">DESCRIPTION</span></span>
<span data-ttu-id="1a069-106">A **New-AzStorageBlobRangeToRestore** parancsmag létrehoz egy Blob-tartomány objektumot, amely használható a Restore-AzStorageBlobRange-ban.</span><span class="sxs-lookup"><span data-stu-id="1a069-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="1a069-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1a069-107">EXAMPLES</span></span>

### <span data-ttu-id="1a069-108">1. példa: Visszaállítható blobtartományt hoz létre</span><span class="sxs-lookup"><span data-stu-id="1a069-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="1a069-109">Ez a parancs létrehoz egy visszaállítandó blobtartományt, amely a container1/blob1 (include) fájllal kezdődik, és a container2/blob2 (kizárva) értéken végződik.</span><span class="sxs-lookup"><span data-stu-id="1a069-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="1a069-110">2. példa: Olyan blobtartományt hoz létre, amely betűrendben visszaállítja az első blobból egy adott blobba (kizárva)</span><span class="sxs-lookup"><span data-stu-id="1a069-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="1a069-111">Ez a parancs létrehoz egy blobtartományt, amely a betűrend szerinti első blobból egy adott blobtárolóba2/blob2-re (kizárva)</span><span class="sxs-lookup"><span data-stu-id="1a069-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="1a069-112">3. példa: Olyan blobtartományt hoz létre, amely egy adott blobból (include) visszaáll az utolsó blobig betűrendben.</span><span class="sxs-lookup"><span data-stu-id="1a069-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="1a069-113">Ezzel a paranccsal olyan blobtartományt hoz létre, amely egy adott blobtárolóból1/blob1-ről (beleértve) az utolsó blobig, betűrendbe rendezve fog visszaállni.</span><span class="sxs-lookup"><span data-stu-id="1a069-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="1a069-114">4. példa: Blobtartományt hoz létre, amely az összes blobot visszaállítja</span><span class="sxs-lookup"><span data-stu-id="1a069-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="1a069-115">Ez a parancs létrehoz egy blobtartományt, amely visszaállítja az összes blobot.</span><span class="sxs-lookup"><span data-stu-id="1a069-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="1a069-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a069-116">PARAMETERS</span></span>

### <span data-ttu-id="1a069-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a069-117">-DefaultProfile</span></span>
<span data-ttu-id="1a069-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a069-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a069-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="1a069-119">-EndRange</span></span>
<span data-ttu-id="1a069-120">Adja meg a blob-visszaállítás záró tartományát.</span><span class="sxs-lookup"><span data-stu-id="1a069-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="1a069-121">A végponttartományt a visszaállítási blobok nem fogják kizárni.</span><span class="sxs-lookup"><span data-stu-id="1a069-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="1a069-122">Állítsa üres strngként a végpontra való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="1a069-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="1a069-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="1a069-123">-StartRange</span></span>
<span data-ttu-id="1a069-124">Adja meg a blob-visszaállítás kezdési tartományát.</span><span class="sxs-lookup"><span data-stu-id="1a069-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="1a069-125">A kezdő tartomány szerepelni fog a visszaállítási blobok között.</span><span class="sxs-lookup"><span data-stu-id="1a069-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="1a069-126">Állítsa be üres karakterláncként az elejétől való visszaállításhoz.</span><span class="sxs-lookup"><span data-stu-id="1a069-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="1a069-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a069-127">CommonParameters</span></span>
<span data-ttu-id="1a069-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a069-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a069-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a069-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a069-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a069-130">INPUTS</span></span>

### <span data-ttu-id="1a069-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="1a069-131">None</span></span>

## <span data-ttu-id="1a069-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a069-132">OUTPUTS</span></span>

### <span data-ttu-id="1a069-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="1a069-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="1a069-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1a069-134">NOTES</span></span>

## <span data-ttu-id="1a069-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a069-135">RELATED LINKS</span></span>
