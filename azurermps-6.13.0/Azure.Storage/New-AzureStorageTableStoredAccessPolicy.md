---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 5a2890f052e57c37ca86197b2fd3841ba3b5c388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502296"
---
# <span data-ttu-id="7fae5-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fae5-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7fae5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7fae5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fae5-103">Egy, az Azure Storage-táblájához tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7fae5-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fae5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7fae5-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fae5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7fae5-105">DESCRIPTION</span></span>
<span data-ttu-id="7fae5-106">A **New-AzureStorageTableStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="7fae5-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="7fae5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7fae5-107">EXAMPLES</span></span>

### <span data-ttu-id="7fae5-108">Példa 1: tárolt hozzáférés-házirend létrehozása táblázatban</span><span class="sxs-lookup"><span data-stu-id="7fae5-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="7fae5-109">A parancs létrehoz egy Policy02 nevű Access-házirendet a táblanév nevű tárterület táblában.</span><span class="sxs-lookup"><span data-stu-id="7fae5-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="7fae5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7fae5-110">PARAMETERS</span></span>

### <span data-ttu-id="7fae5-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7fae5-111">-Context</span></span>
<span data-ttu-id="7fae5-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7fae5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7fae5-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7fae5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fae5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fae5-114">-DefaultProfile</span></span>
<span data-ttu-id="7fae5-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fae5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fae5-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7fae5-116">-ExpiryTime</span></span>
<span data-ttu-id="7fae5-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="7fae5-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae5-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="7fae5-118">-Permission</span></span>
<span data-ttu-id="7fae5-119">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7fae5-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="7fae5-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="7fae5-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae5-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="7fae5-121">-Policy</span></span>
<span data-ttu-id="7fae5-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7fae5-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae5-123">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="7fae5-123">-StartTime</span></span>
<span data-ttu-id="7fae5-124">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="7fae5-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fae5-125">-Table</span><span class="sxs-lookup"><span data-stu-id="7fae5-125">-Table</span></span>
<span data-ttu-id="7fae5-126">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7fae5-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fae5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fae5-127">CommonParameters</span></span>
<span data-ttu-id="7fae5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7fae5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fae5-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fae5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fae5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fae5-130">INPUTS</span></span>

### <span data-ttu-id="7fae5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7fae5-131">System.String</span></span>

### <span data-ttu-id="7fae5-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fae5-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7fae5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fae5-133">OUTPUTS</span></span>

### <span data-ttu-id="7fae5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7fae5-134">System.String</span></span>

## <span data-ttu-id="7fae5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7fae5-135">NOTES</span></span>

## <span data-ttu-id="7fae5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fae5-136">RELATED LINKS</span></span>

[<span data-ttu-id="7fae5-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fae5-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7fae5-138">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7fae5-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="7fae5-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fae5-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7fae5-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7fae5-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


