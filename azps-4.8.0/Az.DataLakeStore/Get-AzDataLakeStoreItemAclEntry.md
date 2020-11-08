---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184575"
---
# <span data-ttu-id="9fcdc-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9fcdc-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="9fcdc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="9fcdc-103">Beilleszt egy bejegyzést az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájába.</span><span class="sxs-lookup"><span data-stu-id="9fcdc-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9fcdc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fcdc-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fcdc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fcdc-105">DESCRIPTION</span></span>
<span data-ttu-id="9fcdc-106">A **Get-AzDataLakeStoreItemAclEntry** parancsmag egy bejegyzés (ACE) beírása az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában.</span><span class="sxs-lookup"><span data-stu-id="9fcdc-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9fcdc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9fcdc-107">EXAMPLES</span></span>

### <span data-ttu-id="9fcdc-108">1. példa: mappa HOZZÁFÉRÉSének beszerzése</span><span class="sxs-lookup"><span data-stu-id="9fcdc-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="9fcdc-109">Ez a parancs beilleszti a megadott Data Lake Store-fiók gyökérkönyvtárának hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="9fcdc-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="9fcdc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fcdc-110">PARAMETERS</span></span>

### <span data-ttu-id="9fcdc-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="9fcdc-111">-Account</span></span>
<span data-ttu-id="9fcdc-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fcdc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9fcdc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fcdc-113">-DefaultProfile</span></span>
<span data-ttu-id="9fcdc-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fcdc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fcdc-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="9fcdc-115">-Path</span></span>
<span data-ttu-id="9fcdc-116">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre ez a parancsmag beilleszti az ACE-t, a gyökérkönyvtártól kezdve</span><span class="sxs-lookup"><span data-stu-id="9fcdc-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9fcdc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fcdc-117">CommonParameters</span></span>
<span data-ttu-id="9fcdc-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fcdc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fcdc-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fcdc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fcdc-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fcdc-120">INPUTS</span></span>

### <span data-ttu-id="9fcdc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9fcdc-121">System.String</span></span>

### <span data-ttu-id="9fcdc-122">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9fcdc-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="9fcdc-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fcdc-123">OUTPUTS</span></span>

### <span data-ttu-id="9fcdc-124">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="9fcdc-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="9fcdc-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fcdc-125">NOTES</span></span>

## <span data-ttu-id="9fcdc-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fcdc-126">RELATED LINKS</span></span>

[<span data-ttu-id="9fcdc-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9fcdc-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="9fcdc-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9fcdc-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


