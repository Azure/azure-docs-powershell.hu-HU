---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671766"
---
# <span data-ttu-id="96618-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96618-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="96618-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96618-102">SYNOPSIS</span></span>
<span data-ttu-id="96618-103">Tárolt hozzáférés-házirendet hoz létre az Azure tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="96618-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="96618-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96618-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="96618-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96618-105">DESCRIPTION</span></span>
<span data-ttu-id="96618-106">A **New-AzureStorageQueueStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="96618-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="96618-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96618-107">EXAMPLES</span></span>

### <span data-ttu-id="96618-108">Példa 1: tárolt hozzáférés-házirend létrehozása tárolási várólistában</span><span class="sxs-lookup"><span data-stu-id="96618-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="96618-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyQueue nevű tárolási várólistában.</span><span class="sxs-lookup"><span data-stu-id="96618-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="96618-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96618-110">PARAMETERS</span></span>

### <span data-ttu-id="96618-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="96618-111">-Context</span></span>
<span data-ttu-id="96618-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96618-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96618-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96618-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="96618-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="96618-114">-ExpiryTime</span></span>
<span data-ttu-id="96618-115">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="96618-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="96618-116">– Engedély</span><span class="sxs-lookup"><span data-stu-id="96618-116">-Permission</span></span>
<span data-ttu-id="96618-117">A tárterület-várólistához való nyilvános hozzáférés szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96618-117">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="96618-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="96618-118">-Policy</span></span>
<span data-ttu-id="96618-119">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="96618-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="96618-120">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="96618-120">-Queue</span></span>
<span data-ttu-id="96618-121">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="96618-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="96618-122">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="96618-122">-StartTime</span></span>
<span data-ttu-id="96618-123">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="96618-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="96618-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96618-124">CommonParameters</span></span>
<span data-ttu-id="96618-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96618-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96618-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96618-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96618-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96618-127">INPUTS</span></span>

## <span data-ttu-id="96618-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96618-128">OUTPUTS</span></span>

## <span data-ttu-id="96618-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96618-129">NOTES</span></span>

## <span data-ttu-id="96618-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96618-130">RELATED LINKS</span></span>

[<span data-ttu-id="96618-131">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96618-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="96618-132">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="96618-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="96618-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96618-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="96618-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96618-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


