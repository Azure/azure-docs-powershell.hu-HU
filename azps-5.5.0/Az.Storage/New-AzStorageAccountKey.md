---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: eebf58120449466ac18231af6daed538ff7da937
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162987"
---
# <span data-ttu-id="adaee-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="adaee-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="adaee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adaee-102">SYNOPSIS</span></span>
<span data-ttu-id="adaee-103">Az Azure Storage-fiók tárkulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="adaee-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="adaee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adaee-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adaee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adaee-105">DESCRIPTION</span></span>
<span data-ttu-id="adaee-106">A **New-AzStorageAccountKey** parancsmag újragenerálja egy Azure Storage-fiók tárkulcsát.</span><span class="sxs-lookup"><span data-stu-id="adaee-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="adaee-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adaee-107">EXAMPLES</span></span>

### <span data-ttu-id="adaee-108">1. példa: Tárkulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="adaee-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="adaee-109">Ez a parancs a megadott tárfiók tárkulcsát újragenerálja.</span><span class="sxs-lookup"><span data-stu-id="adaee-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="adaee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adaee-110">PARAMETERS</span></span>

### <span data-ttu-id="adaee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaee-111">-DefaultProfile</span></span>
<span data-ttu-id="adaee-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adaee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adaee-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="adaee-113">-KeyName</span></span>
<span data-ttu-id="adaee-114">Megadja, hogy melyik kulcsot kell újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="adaee-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="adaee-115">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="adaee-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="adaee-116">billentyű1</span><span class="sxs-lookup"><span data-stu-id="adaee-116">key1</span></span>
- <span data-ttu-id="adaee-117">billentyű2</span><span class="sxs-lookup"><span data-stu-id="adaee-117">key2</span></span>
- <span data-ttu-id="adaee-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="adaee-118">kerb1</span></span>
- <span data-ttu-id="adaee-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="adaee-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adaee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="adaee-120">-Name</span></span>
<span data-ttu-id="adaee-121">Annak a tárfióknak a nevét adja meg, amelynek a tárkulcsát újra létre kell hozni.</span><span class="sxs-lookup"><span data-stu-id="adaee-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adaee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adaee-122">-ResourceGroupName</span></span>
<span data-ttu-id="adaee-123">A Tárfiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="adaee-123">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="adaee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaee-124">CommonParameters</span></span>
<span data-ttu-id="adaee-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adaee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaee-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adaee-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaee-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adaee-127">INPUTS</span></span>

### <span data-ttu-id="adaee-128">System.String</span><span class="sxs-lookup"><span data-stu-id="adaee-128">System.String</span></span>

## <span data-ttu-id="adaee-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adaee-129">OUTPUTS</span></span>

### <span data-ttu-id="adaee-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="adaee-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="adaee-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adaee-131">NOTES</span></span>

## <span data-ttu-id="adaee-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adaee-132">RELATED LINKS</span></span>

[<span data-ttu-id="adaee-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="adaee-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
