---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679463"
---
# <span data-ttu-id="bd750-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bd750-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="bd750-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bd750-102">SYNOPSIS</span></span>
<span data-ttu-id="bd750-103">Beilleszt egy bejegyzést az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájába.</span><span class="sxs-lookup"><span data-stu-id="bd750-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd750-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bd750-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd750-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bd750-105">DESCRIPTION</span></span>
<span data-ttu-id="bd750-106">A **Get-AzureRmDataLakeStoreItemAclEntry** parancsmag egy bejegyzés (ACE) beírása az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában.</span><span class="sxs-lookup"><span data-stu-id="bd750-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bd750-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bd750-107">EXAMPLES</span></span>

### <span data-ttu-id="bd750-108">1. példa: mappa HOZZÁFÉRÉSének beszerzése</span><span class="sxs-lookup"><span data-stu-id="bd750-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="bd750-109">Ez a parancs beilleszti a megadott Data Lake Store-fiók gyökérkönyvtárának hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="bd750-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="bd750-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bd750-110">PARAMETERS</span></span>

### <span data-ttu-id="bd750-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="bd750-111">-Account</span></span>
<span data-ttu-id="bd750-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd750-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd750-113">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="bd750-113">-Path</span></span>
<span data-ttu-id="bd750-114">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre ez a parancsmag beilleszti az ACE-t, a gyökérkönyvtártól kezdve</span><span class="sxs-lookup"><span data-stu-id="bd750-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd750-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd750-115">-DefaultProfile</span></span>
<span data-ttu-id="bd750-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd750-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd750-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd750-117">CommonParameters</span></span>
<span data-ttu-id="bd750-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bd750-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd750-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd750-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd750-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd750-120">INPUTS</span></span>

## <span data-ttu-id="bd750-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd750-121">OUTPUTS</span></span>

### <span data-ttu-id="bd750-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="bd750-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="bd750-123">A megadott mappa vagy fájl ACL-bejegyzéseinek listája.</span><span class="sxs-lookup"><span data-stu-id="bd750-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="bd750-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bd750-124">NOTES</span></span>

## <span data-ttu-id="bd750-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd750-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd750-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bd750-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="bd750-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="bd750-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


