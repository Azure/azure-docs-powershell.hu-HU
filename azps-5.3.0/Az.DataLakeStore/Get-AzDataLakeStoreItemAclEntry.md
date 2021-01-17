---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465838"
---
# <span data-ttu-id="2a493-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2a493-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="2a493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a493-102">SYNOPSIS</span></span>
<span data-ttu-id="2a493-103">Bejegyzést kap a Data Lake Store-ban tárolt fájl vagy mappa ACL-ében.</span><span class="sxs-lookup"><span data-stu-id="2a493-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2a493-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a493-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a493-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a493-105">DESCRIPTION</span></span>
<span data-ttu-id="2a493-106">A **Get-AzDataLakeStoreItemAclEntry** parancsmag a Data Lake Store-ban található fájlok vagy mappák hozzáférés-vezérlési listájában (ACL) kap egy bejegyzést (ACE).</span><span class="sxs-lookup"><span data-stu-id="2a493-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2a493-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a493-107">EXAMPLES</span></span>

### <span data-ttu-id="2a493-108">1. példa: Mappa ACL-ének lekérte</span><span class="sxs-lookup"><span data-stu-id="2a493-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="2a493-109">Ez a parancs lekérte a megadott Data Lake Store-fiók gyökérkönyvtárának ACL-ét</span><span class="sxs-lookup"><span data-stu-id="2a493-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="2a493-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a493-110">PARAMETERS</span></span>

### <span data-ttu-id="2a493-111">-Account</span><span class="sxs-lookup"><span data-stu-id="2a493-111">-Account</span></span>
<span data-ttu-id="2a493-112">A Data Lake Store-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a493-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2a493-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a493-113">-DefaultProfile</span></span>
<span data-ttu-id="2a493-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a493-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a493-115">-Path</span><span class="sxs-lookup"><span data-stu-id="2a493-115">-Path</span></span>
<span data-ttu-id="2a493-116">Annak az elemnek a Data Lake Store-beli elérési útját adja meg, amelynek a parancsmagja ACE-et kap, a gyökérkönyvtártól (/).</span><span class="sxs-lookup"><span data-stu-id="2a493-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2a493-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a493-117">CommonParameters</span></span>
<span data-ttu-id="2a493-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a493-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a493-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a493-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a493-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a493-120">INPUTS</span></span>

### <span data-ttu-id="2a493-121">System.String</span><span class="sxs-lookup"><span data-stu-id="2a493-121">System.String</span></span>

### <span data-ttu-id="2a493-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2a493-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="2a493-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a493-123">OUTPUTS</span></span>

### <span data-ttu-id="2a493-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="2a493-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="2a493-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a493-125">NOTES</span></span>

## <span data-ttu-id="2a493-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a493-126">RELATED LINKS</span></span>

[<span data-ttu-id="2a493-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2a493-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="2a493-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2a493-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


