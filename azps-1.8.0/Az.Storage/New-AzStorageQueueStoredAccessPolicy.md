---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 39e83844898771d25c5e2f8a62e4814b36b5e85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668605"
---
# <span data-ttu-id="e4109-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4109-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e4109-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4109-102">SYNOPSIS</span></span>
<span data-ttu-id="e4109-103">Tárolt hozzáférés-házirendet hoz létre az Azure tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="e4109-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e4109-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4109-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4109-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4109-105">DESCRIPTION</span></span>
<span data-ttu-id="e4109-106">A **New-AzStorageQueueStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="e4109-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e4109-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4109-107">EXAMPLES</span></span>

### <span data-ttu-id="e4109-108">Példa 1: tárolt hozzáférés-házirend létrehozása tárolási várólistában</span><span class="sxs-lookup"><span data-stu-id="e4109-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="e4109-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyQueue nevű tárolási várólistában.</span><span class="sxs-lookup"><span data-stu-id="e4109-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="e4109-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4109-110">PARAMETERS</span></span>

### <span data-ttu-id="e4109-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e4109-111">-Context</span></span>
<span data-ttu-id="e4109-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4109-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e4109-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e4109-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e4109-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4109-114">-DefaultProfile</span></span>
<span data-ttu-id="e4109-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4109-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4109-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e4109-116">-ExpiryTime</span></span>
<span data-ttu-id="e4109-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="e4109-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="e4109-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="e4109-118">-Permission</span></span>
<span data-ttu-id="e4109-119">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="e4109-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="e4109-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="e4109-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="e4109-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e4109-121">-Policy</span></span>
<span data-ttu-id="e4109-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4109-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="e4109-123">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="e4109-123">-Queue</span></span>
<span data-ttu-id="e4109-124">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4109-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e4109-125">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="e4109-125">-StartTime</span></span>
<span data-ttu-id="e4109-126">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="e4109-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="e4109-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4109-127">CommonParameters</span></span>
<span data-ttu-id="e4109-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4109-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4109-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4109-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4109-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4109-130">INPUTS</span></span>

### <span data-ttu-id="e4109-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e4109-131">System.String</span></span>

### <span data-ttu-id="e4109-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e4109-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e4109-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4109-133">OUTPUTS</span></span>

### <span data-ttu-id="e4109-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e4109-134">System.String</span></span>

## <span data-ttu-id="e4109-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4109-135">NOTES</span></span>

## <span data-ttu-id="e4109-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4109-136">RELATED LINKS</span></span>

[<span data-ttu-id="e4109-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4109-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e4109-138">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e4109-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="e4109-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4109-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e4109-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4109-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


