---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 8473cc65ec6afffb9433159d848d9e7b8629a351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499559"
---
# <span data-ttu-id="a74ec-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a74ec-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="a74ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a74ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a74ec-103">Beilleszt egy bejegyzést az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájába.</span><span class="sxs-lookup"><span data-stu-id="a74ec-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a74ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a74ec-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a74ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a74ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a74ec-106">A **Get-AzureRmDataLakeStoreItemAclEntry** parancsmag egy bejegyzés (ACE) beírása az adattó-tárolóban lévő fájlok vagy mappák hozzáférés-vezérlési listájában.</span><span class="sxs-lookup"><span data-stu-id="a74ec-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a74ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a74ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a74ec-108">1. példa: mappa HOZZÁFÉRÉSének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a74ec-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="a74ec-109">Ez a parancs beilleszti a megadott Data Lake Store-fiók gyökérkönyvtárának hozzáférés-vezérlési listáját.</span><span class="sxs-lookup"><span data-stu-id="a74ec-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="a74ec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a74ec-110">PARAMETERS</span></span>

### <span data-ttu-id="a74ec-111">-Fiók</span><span class="sxs-lookup"><span data-stu-id="a74ec-111">-Account</span></span>
<span data-ttu-id="a74ec-112">Az adattó-tároló fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a74ec-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a74ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74ec-113">-DefaultProfile</span></span>
<span data-ttu-id="a74ec-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a74ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a74ec-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a74ec-115">-Path</span></span>
<span data-ttu-id="a74ec-116">Itt adhatja meg az adattó-tároló elérési útját annak az elemnek az elérési útjával, amelyre ez a parancsmag beilleszti az ACE-t, a gyökérkönyvtártól kezdve</span><span class="sxs-lookup"><span data-stu-id="a74ec-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a74ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74ec-117">CommonParameters</span></span>
<span data-ttu-id="a74ec-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a74ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74ec-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74ec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74ec-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a74ec-120">INPUTS</span></span>

### <span data-ttu-id="a74ec-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a74ec-121">System.String</span></span>

### <span data-ttu-id="a74ec-122">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a74ec-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="a74ec-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a74ec-123">OUTPUTS</span></span>

### <span data-ttu-id="a74ec-124">Microsoft. Azure. Command. DataLakeStore. models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="a74ec-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="a74ec-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a74ec-125">NOTES</span></span>

## <span data-ttu-id="a74ec-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a74ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="a74ec-127">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a74ec-127">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="a74ec-128">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="a74ec-128">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


