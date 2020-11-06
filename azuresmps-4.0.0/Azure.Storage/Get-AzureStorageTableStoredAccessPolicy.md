---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491714"
---
# <span data-ttu-id="04b8b-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04b8b-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="04b8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="04b8b-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure Storage table.</span><span class="sxs-lookup"><span data-stu-id="04b8b-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="04b8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04b8b-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="04b8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="04b8b-106">A **Get-AzureStorageTableStoredAccessPolicy** parancsmag felsorolja az Azure Storage Tables tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="04b8b-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="04b8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="04b8b-107">EXAMPLES</span></span>

### <span data-ttu-id="04b8b-108">Példa 1: tárolt hozzáférés-házirend beszerzése tárterület-táblában</span><span class="sxs-lookup"><span data-stu-id="04b8b-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="04b8b-109">Ez a parancs a Policy50 nevű Access-házirendet a Table02 nevű tárolási táblában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="04b8b-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="04b8b-110">2. példa: az összes tárolt Access-házirend beolvasása egy tárterület-táblában</span><span class="sxs-lookup"><span data-stu-id="04b8b-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="04b8b-111">Ez a parancs a Table02 nevű táblázat minden hozzáférési házirendjét bekapja.</span><span class="sxs-lookup"><span data-stu-id="04b8b-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="04b8b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04b8b-112">PARAMETERS</span></span>

### <span data-ttu-id="04b8b-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="04b8b-113">-Context</span></span>
<span data-ttu-id="04b8b-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04b8b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="04b8b-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="04b8b-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04b8b-116">-Házirend</span><span class="sxs-lookup"><span data-stu-id="04b8b-116">-Policy</span></span>
<span data-ttu-id="04b8b-117">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="04b8b-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b8b-118">-Table</span><span class="sxs-lookup"><span data-stu-id="04b8b-118">-Table</span></span>
<span data-ttu-id="04b8b-119">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04b8b-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04b8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b8b-120">CommonParameters</span></span>
<span data-ttu-id="04b8b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04b8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b8b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b8b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b8b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04b8b-123">INPUTS</span></span>

## <span data-ttu-id="04b8b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04b8b-124">OUTPUTS</span></span>

## <span data-ttu-id="04b8b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04b8b-125">NOTES</span></span>

## <span data-ttu-id="04b8b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04b8b-126">RELATED LINKS</span></span>

[<span data-ttu-id="04b8b-127">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04b8b-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04b8b-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04b8b-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04b8b-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="04b8b-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="04b8b-130">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="04b8b-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


