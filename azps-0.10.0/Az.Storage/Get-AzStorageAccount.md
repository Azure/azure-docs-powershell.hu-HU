---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: be32e761fc854c6ad4a270f36e4c9b6328e00ba1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843126"
---
# <span data-ttu-id="e5c6d-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6d-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="e5c6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c6d-103">Megkapja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-103">Gets a Storage account.</span></span>

## <span data-ttu-id="e5c6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5c6d-104">SYNTAX</span></span>

### <span data-ttu-id="e5c6d-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c6d-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c6d-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c6d-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c6d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5c6d-107">DESCRIPTION</span></span>
<span data-ttu-id="e5c6d-108">A **Get-AzStorageAccount** parancsmag egy erőforrás-csoportban vagy az előfizetésben megadott tárolási fiókot vagy minden tárolási fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="e5c6d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e5c6d-109">EXAMPLES</span></span>

### <span data-ttu-id="e5c6d-110">1. példa: megadott tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="e5c6d-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="e5c6d-111">Ez a parancs a megadott tárterület-fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="e5c6d-112">2. példa: az erőforráscsoport minden tárolási fiókjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e5c6d-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="e5c6d-113">Ez a parancs egy erőforráscsoport minden tárolási fiókját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="e5c6d-114">3. példa: az előfizetésben lévő összes tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="e5c6d-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="e5c6d-115">Ez a parancs az előfizetésben szereplő összes tárolási fiókot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="e5c6d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5c6d-116">PARAMETERS</span></span>

### <span data-ttu-id="e5c6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c6d-117">-DefaultProfile</span></span>
<span data-ttu-id="e5c6d-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c6d-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5c6d-119">-Name</span></span>
<span data-ttu-id="e5c6d-120">A beszerzéshez használandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c6d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c6d-121">-ResourceGroupName</span></span>
<span data-ttu-id="e5c6d-122">Annak a csoportnak a neve, amely a beszerzéshez használt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e5c6d-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c6d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c6d-123">CommonParameters</span></span>
<span data-ttu-id="e5c6d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5c6d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c6d-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c6d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c6d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5c6d-126">INPUTS</span></span>

### <span data-ttu-id="e5c6d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e5c6d-127">System.String</span></span>

## <span data-ttu-id="e5c6d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5c6d-128">OUTPUTS</span></span>

### <span data-ttu-id="e5c6d-129">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6d-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e5c6d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5c6d-130">NOTES</span></span>

## <span data-ttu-id="e5c6d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5c6d-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5c6d-132">Új – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6d-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="e5c6d-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6d-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="e5c6d-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e5c6d-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


