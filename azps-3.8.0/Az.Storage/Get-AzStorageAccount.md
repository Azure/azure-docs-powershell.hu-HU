---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: db0c0672a6f60aa8c46f85a98e74f5184842cd72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012299"
---
# <span data-ttu-id="48853-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48853-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="48853-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48853-102">SYNOPSIS</span></span>
<span data-ttu-id="48853-103">Megkapja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="48853-103">Gets a Storage account.</span></span>

## <span data-ttu-id="48853-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48853-104">SYNTAX</span></span>

### <span data-ttu-id="48853-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="48853-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48853-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="48853-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48853-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="48853-107">DESCRIPTION</span></span>
<span data-ttu-id="48853-108">A **Get-AzStorageAccount** parancsmag egy erőforrás-csoportban vagy az előfizetésben megadott tárolási fiókot vagy minden tárolási fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="48853-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="48853-109">Példák</span><span class="sxs-lookup"><span data-stu-id="48853-109">EXAMPLES</span></span>

### <span data-ttu-id="48853-110">1. példa: megadott tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="48853-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="48853-111">Ez a parancs a megadott tárterület-fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="48853-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="48853-112">2. példa: az erőforráscsoport minden tárolási fiókjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="48853-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="48853-113">Ez a parancs egy erőforráscsoport minden tárolási fiókját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="48853-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="48853-114">3. példa: az előfizetésben lévő összes tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="48853-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="48853-115">Ez a parancs az előfizetésben szereplő összes tárolási fiókot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="48853-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="48853-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48853-116">PARAMETERS</span></span>

### <span data-ttu-id="48853-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48853-117">-DefaultProfile</span></span>
<span data-ttu-id="48853-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48853-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48853-119">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="48853-119">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="48853-120">A GeoReplicationStats beszerzése</span><span class="sxs-lookup"><span data-stu-id="48853-120">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48853-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="48853-121">-Name</span></span>
<span data-ttu-id="48853-122">A beszerzéshez használandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="48853-122">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="48853-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48853-123">-ResourceGroupName</span></span>
<span data-ttu-id="48853-124">Annak a csoportnak a neve, amely a beszerzéshez használt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="48853-124">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="48853-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48853-125">CommonParameters</span></span>
<span data-ttu-id="48853-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48853-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48853-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48853-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48853-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48853-128">INPUTS</span></span>

### <span data-ttu-id="48853-129">System. String</span><span class="sxs-lookup"><span data-stu-id="48853-129">System.String</span></span>

## <span data-ttu-id="48853-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48853-130">OUTPUTS</span></span>

### <span data-ttu-id="48853-131">Microsoft. Azure. Command. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48853-131">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="48853-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48853-132">NOTES</span></span>

## <span data-ttu-id="48853-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48853-133">RELATED LINKS</span></span>

[<span data-ttu-id="48853-134">Új – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48853-134">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="48853-135">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48853-135">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="48853-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48853-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


