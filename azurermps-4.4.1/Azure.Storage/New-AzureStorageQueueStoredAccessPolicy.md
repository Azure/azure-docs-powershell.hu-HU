---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: ef54976ed06eb47da803470a3d4c163a8b294743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505708"
---
# <span data-ttu-id="882a5-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="882a5-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="882a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="882a5-102">SYNOPSIS</span></span>
<span data-ttu-id="882a5-103">Tárolt hozzáférés-házirendet hoz létre az Azure tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="882a5-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="882a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="882a5-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="882a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="882a5-105">DESCRIPTION</span></span>
<span data-ttu-id="882a5-106">A **New-AzureStorageQueueStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="882a5-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="882a5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="882a5-107">EXAMPLES</span></span>

### <span data-ttu-id="882a5-108">Példa 1: tárolt hozzáférés-házirend létrehozása tárolási várólistában</span><span class="sxs-lookup"><span data-stu-id="882a5-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="882a5-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyQueue nevű tárolási várólistában.</span><span class="sxs-lookup"><span data-stu-id="882a5-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="882a5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="882a5-110">PARAMETERS</span></span>

### <span data-ttu-id="882a5-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="882a5-111">-Context</span></span>
<span data-ttu-id="882a5-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="882a5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="882a5-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="882a5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="882a5-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="882a5-114">-ExpiryTime</span></span>
<span data-ttu-id="882a5-115">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="882a5-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="882a5-116">– Engedély</span><span class="sxs-lookup"><span data-stu-id="882a5-116">-Permission</span></span>
<span data-ttu-id="882a5-117">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="882a5-117">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="882a5-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="882a5-118">-Policy</span></span>
<span data-ttu-id="882a5-119">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="882a5-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="882a5-120">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="882a5-120">-Queue</span></span>
<span data-ttu-id="882a5-121">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="882a5-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="882a5-122">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="882a5-122">-StartTime</span></span>
<span data-ttu-id="882a5-123">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="882a5-123">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="882a5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882a5-124">CommonParameters</span></span>
<span data-ttu-id="882a5-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="882a5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882a5-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882a5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882a5-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="882a5-127">INPUTS</span></span>

### <span data-ttu-id="882a5-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="882a5-128">IStorageContext</span></span>

<span data-ttu-id="882a5-129">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="882a5-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="882a5-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="882a5-130">String</span></span>

<span data-ttu-id="882a5-131">A "várólista" paraméter a folyamat "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="882a5-131">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="882a5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="882a5-132">OUTPUTS</span></span>

### <span data-ttu-id="882a5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="882a5-133">System.String</span></span>

## <span data-ttu-id="882a5-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="882a5-134">NOTES</span></span>

## <span data-ttu-id="882a5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="882a5-135">RELATED LINKS</span></span>

[<span data-ttu-id="882a5-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="882a5-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="882a5-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="882a5-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="882a5-138">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="882a5-138">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="882a5-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="882a5-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


