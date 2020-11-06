---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ea317e4fba3a1c92b55a4cab1acb46873b1d5c92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498616"
---
# <span data-ttu-id="81b02-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81b02-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="81b02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81b02-102">SYNOPSIS</span></span>
<span data-ttu-id="81b02-103">Tárolt hozzáférés-házirendet hoz létre az Azure tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="81b02-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81b02-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81b02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="81b02-105">DESCRIPTION</span></span>
<span data-ttu-id="81b02-106">A **New-AzureStorageQueueStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="81b02-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="81b02-107">Példák</span><span class="sxs-lookup"><span data-stu-id="81b02-107">EXAMPLES</span></span>

### <span data-ttu-id="81b02-108">Példa 1: tárolt hozzáférés-házirend létrehozása tárolási várólistában</span><span class="sxs-lookup"><span data-stu-id="81b02-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="81b02-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyQueue nevű tárolási várólistában.</span><span class="sxs-lookup"><span data-stu-id="81b02-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="81b02-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81b02-110">PARAMETERS</span></span>

### <span data-ttu-id="81b02-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="81b02-111">-Context</span></span>
<span data-ttu-id="81b02-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81b02-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="81b02-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="81b02-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="81b02-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b02-114">-DefaultProfile</span></span>
<span data-ttu-id="81b02-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81b02-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b02-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="81b02-116">-ExpiryTime</span></span>
<span data-ttu-id="81b02-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="81b02-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="81b02-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="81b02-118">-Permission</span></span>
<span data-ttu-id="81b02-119">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="81b02-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="81b02-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="81b02-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="81b02-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="81b02-121">-Policy</span></span>
<span data-ttu-id="81b02-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="81b02-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="81b02-123">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="81b02-123">-Queue</span></span>
<span data-ttu-id="81b02-124">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="81b02-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="81b02-125">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="81b02-125">-StartTime</span></span>
<span data-ttu-id="81b02-126">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="81b02-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="81b02-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b02-127">CommonParameters</span></span>
<span data-ttu-id="81b02-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81b02-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b02-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b02-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b02-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81b02-130">INPUTS</span></span>

### <span data-ttu-id="81b02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="81b02-131">System.String</span></span>

### <span data-ttu-id="81b02-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="81b02-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="81b02-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81b02-133">OUTPUTS</span></span>

### <span data-ttu-id="81b02-134">System. String</span><span class="sxs-lookup"><span data-stu-id="81b02-134">System.String</span></span>

## <span data-ttu-id="81b02-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81b02-135">NOTES</span></span>

## <span data-ttu-id="81b02-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81b02-136">RELATED LINKS</span></span>

[<span data-ttu-id="81b02-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81b02-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="81b02-138">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="81b02-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="81b02-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81b02-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="81b02-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="81b02-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


