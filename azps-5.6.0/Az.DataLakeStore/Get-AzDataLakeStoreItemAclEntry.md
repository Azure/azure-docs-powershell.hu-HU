---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 76d745c16dae7fdfae7feca46c3b32715fa82f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940514"
---
# <span data-ttu-id="726c3-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="726c3-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="726c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="726c3-102">SYNOPSIS</span></span>
<span data-ttu-id="726c3-103">Bejegyzést kap a Data Lake Store-ban tárolt fájl vagy mappa ACL-ében.</span><span class="sxs-lookup"><span data-stu-id="726c3-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="726c3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="726c3-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="726c3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="726c3-105">DESCRIPTION</span></span>
<span data-ttu-id="726c3-106">A **Get-AzDataLakeStoreItemAclEntry** parancsmag a Data Lake Store-ban található fájlok vagy mappák hozzáférés-vezérlési listájában (ACL) kap egy bejegyzést (ACE).</span><span class="sxs-lookup"><span data-stu-id="726c3-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="726c3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="726c3-107">EXAMPLES</span></span>

### <span data-ttu-id="726c3-108">1. példa: Mappa ACL-ének lekérte</span><span class="sxs-lookup"><span data-stu-id="726c3-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="726c3-109">Ez a parancs lekérte a megadott Data Lake Store-fiók gyökérkönyvtárának ACL-ét</span><span class="sxs-lookup"><span data-stu-id="726c3-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="726c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="726c3-110">PARAMETERS</span></span>

### <span data-ttu-id="726c3-111">-Account</span><span class="sxs-lookup"><span data-stu-id="726c3-111">-Account</span></span>
<span data-ttu-id="726c3-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="726c3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="726c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726c3-113">-DefaultProfile</span></span>
<span data-ttu-id="726c3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="726c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="726c3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="726c3-115">-Path</span></span>
<span data-ttu-id="726c3-116">Annak az elemnek a Data Lake Store-beli elérési útját adja meg, amelynek a parancsmagja ACE-et kap, a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="726c3-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="726c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726c3-117">CommonParameters</span></span>
<span data-ttu-id="726c3-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726c3-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="726c3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726c3-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="726c3-120">INPUTS</span></span>

### <span data-ttu-id="726c3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="726c3-121">System.String</span></span>

### <span data-ttu-id="726c3-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="726c3-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="726c3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="726c3-123">OUTPUTS</span></span>

### <span data-ttu-id="726c3-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="726c3-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="726c3-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="726c3-125">NOTES</span></span>

## <span data-ttu-id="726c3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="726c3-126">RELATED LINKS</span></span>

[<span data-ttu-id="726c3-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="726c3-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="726c3-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="726c3-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


