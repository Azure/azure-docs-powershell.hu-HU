---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490791"
---
# <span data-ttu-id="73325-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73325-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="73325-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73325-102">SYNOPSIS</span></span>
<span data-ttu-id="73325-103">Egy, az Azure Storage-táblájához tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="73325-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="73325-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73325-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="73325-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73325-105">DESCRIPTION</span></span>
<span data-ttu-id="73325-106">A **New-AzureStorageTableStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="73325-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="73325-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73325-107">EXAMPLES</span></span>

### <span data-ttu-id="73325-108">Példa 1: tárolt hozzáférés-házirend létrehozása táblázatban</span><span class="sxs-lookup"><span data-stu-id="73325-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="73325-109">A parancs létrehoz egy Policy02 nevű Access-házirendet a táblanév nevű tárterület táblában.</span><span class="sxs-lookup"><span data-stu-id="73325-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="73325-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73325-110">PARAMETERS</span></span>

### <span data-ttu-id="73325-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="73325-111">-Context</span></span>
<span data-ttu-id="73325-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73325-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="73325-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="73325-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="73325-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="73325-114">-ExpiryTime</span></span>
<span data-ttu-id="73325-115">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="73325-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73325-116">– Engedély</span><span class="sxs-lookup"><span data-stu-id="73325-116">-Permission</span></span>
<span data-ttu-id="73325-117">A tárterület-tábla nyilvános hozzáférésének szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73325-117">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73325-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="73325-118">-Policy</span></span>
<span data-ttu-id="73325-119">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="73325-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73325-120">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="73325-120">-StartTime</span></span>
<span data-ttu-id="73325-121">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="73325-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73325-122">-Table</span><span class="sxs-lookup"><span data-stu-id="73325-122">-Table</span></span>
<span data-ttu-id="73325-123">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73325-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="73325-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73325-124">CommonParameters</span></span>
<span data-ttu-id="73325-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73325-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73325-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73325-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73325-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73325-127">INPUTS</span></span>

## <span data-ttu-id="73325-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73325-128">OUTPUTS</span></span>

## <span data-ttu-id="73325-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73325-129">NOTES</span></span>

## <span data-ttu-id="73325-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73325-130">RELATED LINKS</span></span>

[<span data-ttu-id="73325-131">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73325-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="73325-132">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="73325-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="73325-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73325-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="73325-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="73325-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


