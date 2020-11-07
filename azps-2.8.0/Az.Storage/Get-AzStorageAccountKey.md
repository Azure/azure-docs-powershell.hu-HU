---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 75ec5690c3699ce8812383ddd128803bf662e489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839643"
---
# <span data-ttu-id="007ae-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="007ae-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="007ae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="007ae-102">SYNOPSIS</span></span>
<span data-ttu-id="007ae-103">Egy Azure-tárterülethez tartozó hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="007ae-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="007ae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="007ae-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="007ae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="007ae-105">DESCRIPTION</span></span>
<span data-ttu-id="007ae-106">A **Get-AzStorageAccountKey** parancsmag a hozzáférési kulcsokat kapja meg egy Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="007ae-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="007ae-107">Példák</span><span class="sxs-lookup"><span data-stu-id="007ae-107">EXAMPLES</span></span>

### <span data-ttu-id="007ae-108">Példa 1: a tárolási fiók hozzáférési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="007ae-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="007ae-109">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="007ae-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="007ae-110">2. példa: speciális hozzáférési kulcs beszerzése tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="007ae-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="007ae-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="007ae-111">PARAMETERS</span></span>

### <span data-ttu-id="007ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007ae-112">-DefaultProfile</span></span>
<span data-ttu-id="007ae-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="007ae-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="007ae-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="007ae-114">-Name</span></span>
<span data-ttu-id="007ae-115">Annak a tároló fióknak a nevét adja meg, amelyhez ez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="007ae-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="007ae-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="007ae-116">-ResourceGroupName</span></span>
<span data-ttu-id="007ae-117">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="007ae-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="007ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007ae-118">CommonParameters</span></span>
<span data-ttu-id="007ae-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="007ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007ae-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="007ae-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007ae-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="007ae-121">INPUTS</span></span>

### <span data-ttu-id="007ae-122">System. String</span><span class="sxs-lookup"><span data-stu-id="007ae-122">System.String</span></span>

## <span data-ttu-id="007ae-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="007ae-123">OUTPUTS</span></span>

### <span data-ttu-id="007ae-124">Microsoft. Azure. Management. Storage. models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="007ae-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="007ae-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="007ae-125">NOTES</span></span>

## <span data-ttu-id="007ae-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="007ae-126">RELATED LINKS</span></span>

[<span data-ttu-id="007ae-127">Új – AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="007ae-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


