---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195049"
---
# <span data-ttu-id="94c25-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="94c25-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="94c25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94c25-102">SYNOPSIS</span></span>
<span data-ttu-id="94c25-103">Egy, az Azure Storage-táblájához tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="94c25-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="94c25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94c25-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94c25-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94c25-105">DESCRIPTION</span></span>
<span data-ttu-id="94c25-106">A **New-AzStorageTableStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="94c25-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="94c25-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94c25-107">EXAMPLES</span></span>

### <span data-ttu-id="94c25-108">Példa 1: tárolt hozzáférés-házirend létrehozása táblázatban</span><span class="sxs-lookup"><span data-stu-id="94c25-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="94c25-109">A parancs létrehoz egy Policy02 nevű Access-házirendet a táblanév nevű tárterület táblában.</span><span class="sxs-lookup"><span data-stu-id="94c25-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="94c25-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94c25-110">PARAMETERS</span></span>

### <span data-ttu-id="94c25-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="94c25-111">-Context</span></span>
<span data-ttu-id="94c25-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94c25-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="94c25-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="94c25-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="94c25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c25-114">-DefaultProfile</span></span>
<span data-ttu-id="94c25-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94c25-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94c25-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="94c25-116">-ExpiryTime</span></span>
<span data-ttu-id="94c25-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="94c25-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="94c25-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="94c25-118">-Permission</span></span>
<span data-ttu-id="94c25-119">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="94c25-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="94c25-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="94c25-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="94c25-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="94c25-121">-Policy</span></span>
<span data-ttu-id="94c25-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94c25-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="94c25-123">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="94c25-123">-StartTime</span></span>
<span data-ttu-id="94c25-124">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="94c25-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="94c25-125">-Table</span><span class="sxs-lookup"><span data-stu-id="94c25-125">-Table</span></span>
<span data-ttu-id="94c25-126">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94c25-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="94c25-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c25-127">CommonParameters</span></span>
<span data-ttu-id="94c25-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94c25-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c25-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c25-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c25-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94c25-130">INPUTS</span></span>

### <span data-ttu-id="94c25-131">System. String</span><span class="sxs-lookup"><span data-stu-id="94c25-131">System.String</span></span>

### <span data-ttu-id="94c25-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="94c25-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="94c25-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94c25-133">OUTPUTS</span></span>

### <span data-ttu-id="94c25-134">System. String</span><span class="sxs-lookup"><span data-stu-id="94c25-134">System.String</span></span>

## <span data-ttu-id="94c25-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94c25-135">NOTES</span></span>

## <span data-ttu-id="94c25-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94c25-136">RELATED LINKS</span></span>

[<span data-ttu-id="94c25-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="94c25-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="94c25-138">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="94c25-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="94c25-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="94c25-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="94c25-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="94c25-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


