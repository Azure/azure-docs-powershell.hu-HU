---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 163c6ba0841b19edc76421259b1cd9cc8411e35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496712"
---
# <span data-ttu-id="8e334-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e334-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="8e334-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e334-102">SYNOPSIS</span></span>
<span data-ttu-id="8e334-103">Egy, az Azure Storage-táblájához tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8e334-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e334-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e334-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8e334-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e334-105">DESCRIPTION</span></span>
<span data-ttu-id="8e334-106">A **New-AzureStorageTableStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="8e334-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="8e334-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8e334-107">EXAMPLES</span></span>

### <span data-ttu-id="8e334-108">Példa 1: tárolt hozzáférés-házirend létrehozása táblázatban</span><span class="sxs-lookup"><span data-stu-id="8e334-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="8e334-109">A parancs létrehoz egy Policy02 nevű Access-házirendet a táblanév nevű tárterület táblában.</span><span class="sxs-lookup"><span data-stu-id="8e334-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="8e334-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e334-110">PARAMETERS</span></span>

### <span data-ttu-id="8e334-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8e334-111">-Context</span></span>
<span data-ttu-id="8e334-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e334-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8e334-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8e334-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8e334-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8e334-114">-ExpiryTime</span></span>
<span data-ttu-id="8e334-115">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="8e334-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="8e334-116">– Engedély</span><span class="sxs-lookup"><span data-stu-id="8e334-116">-Permission</span></span>
<span data-ttu-id="8e334-117">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8e334-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="8e334-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8e334-118">-Policy</span></span>
<span data-ttu-id="8e334-119">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e334-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="8e334-120">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="8e334-120">-StartTime</span></span>
<span data-ttu-id="8e334-121">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="8e334-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8e334-122">-Table</span><span class="sxs-lookup"><span data-stu-id="8e334-122">-Table</span></span>
<span data-ttu-id="8e334-123">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e334-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="8e334-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e334-124">CommonParameters</span></span>
<span data-ttu-id="8e334-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e334-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e334-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e334-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e334-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e334-127">INPUTS</span></span>

### <span data-ttu-id="8e334-128">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8e334-128">IStorageContext</span></span>

<span data-ttu-id="8e334-129">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8e334-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8e334-130">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8e334-130">String</span></span>

<span data-ttu-id="8e334-131">A ' Table ' paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8e334-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8e334-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e334-132">OUTPUTS</span></span>

### <span data-ttu-id="8e334-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8e334-133">System.String</span></span>

## <span data-ttu-id="8e334-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e334-134">NOTES</span></span>

## <span data-ttu-id="8e334-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e334-135">RELATED LINKS</span></span>

[<span data-ttu-id="8e334-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e334-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8e334-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8e334-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8e334-138">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e334-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8e334-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8e334-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


