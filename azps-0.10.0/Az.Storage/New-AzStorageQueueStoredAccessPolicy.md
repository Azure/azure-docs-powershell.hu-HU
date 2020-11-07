---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: cda91974a8498e26f57d3a30381fe97791b2d354
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842982"
---
# <span data-ttu-id="db315-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="db315-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="db315-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db315-102">SYNOPSIS</span></span>
<span data-ttu-id="db315-103">Tárolt hozzáférés-házirendet hoz létre az Azure tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="db315-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="db315-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db315-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db315-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db315-105">DESCRIPTION</span></span>
<span data-ttu-id="db315-106">A **New-AzStorageQueueStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="db315-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="db315-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db315-107">EXAMPLES</span></span>

### <span data-ttu-id="db315-108">Példa 1: tárolt hozzáférés-házirend létrehozása tárolási várólistában</span><span class="sxs-lookup"><span data-stu-id="db315-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="db315-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyQueue nevű tárolási várólistában.</span><span class="sxs-lookup"><span data-stu-id="db315-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="db315-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db315-110">PARAMETERS</span></span>

### <span data-ttu-id="db315-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="db315-111">-Context</span></span>
<span data-ttu-id="db315-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db315-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="db315-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db315-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="db315-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db315-114">-DefaultProfile</span></span>
<span data-ttu-id="db315-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db315-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db315-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="db315-116">-ExpiryTime</span></span>
<span data-ttu-id="db315-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="db315-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="db315-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="db315-118">-Permission</span></span>
<span data-ttu-id="db315-119">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="db315-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="db315-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="db315-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="db315-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="db315-121">-Policy</span></span>
<span data-ttu-id="db315-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db315-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="db315-123">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="db315-123">-Queue</span></span>
<span data-ttu-id="db315-124">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="db315-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="db315-125">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="db315-125">-StartTime</span></span>
<span data-ttu-id="db315-126">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="db315-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="db315-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db315-127">CommonParameters</span></span>
<span data-ttu-id="db315-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db315-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db315-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db315-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db315-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db315-130">INPUTS</span></span>

### <span data-ttu-id="db315-131">System. String</span><span class="sxs-lookup"><span data-stu-id="db315-131">System.String</span></span>

### <span data-ttu-id="db315-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="db315-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="db315-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db315-133">OUTPUTS</span></span>

### <span data-ttu-id="db315-134">System. String</span><span class="sxs-lookup"><span data-stu-id="db315-134">System.String</span></span>

## <span data-ttu-id="db315-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db315-135">NOTES</span></span>

## <span data-ttu-id="db315-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db315-136">RELATED LINKS</span></span>

[<span data-ttu-id="db315-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="db315-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="db315-138">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="db315-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="db315-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="db315-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="db315-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="db315-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


