---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 21e289ce0a8e7ca2d430d64ab9cc75bfd0c1a3ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850502"
---
# <span data-ttu-id="88b6c-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88b6c-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="88b6c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="88b6c-103">Egy, az Azure Storage-táblájához tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="88b6c-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88b6c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88b6c-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b6c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="88b6c-106">A **New-AzureStorageTableStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="88b6c-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="88b6c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="88b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="88b6c-108">Példa 1: tárolt hozzáférés-házirend létrehozása táblázatban</span><span class="sxs-lookup"><span data-stu-id="88b6c-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="88b6c-109">A parancs létrehoz egy Policy02 nevű Access-házirendet a táblanév nevű tárterület táblában.</span><span class="sxs-lookup"><span data-stu-id="88b6c-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="88b6c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="88b6c-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="88b6c-111">-Context</span></span>
<span data-ttu-id="88b6c-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88b6c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="88b6c-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="88b6c-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="88b6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b6c-114">-DefaultProfile</span></span>
<span data-ttu-id="88b6c-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88b6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b6c-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88b6c-116">-ExpiryTime</span></span>
<span data-ttu-id="88b6c-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="88b6c-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="88b6c-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="88b6c-118">-Permission</span></span>
<span data-ttu-id="88b6c-119">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="88b6c-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="88b6c-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="88b6c-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="88b6c-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="88b6c-121">-Policy</span></span>
<span data-ttu-id="88b6c-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88b6c-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="88b6c-123">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="88b6c-123">-StartTime</span></span>
<span data-ttu-id="88b6c-124">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="88b6c-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="88b6c-125">-Table</span><span class="sxs-lookup"><span data-stu-id="88b6c-125">-Table</span></span>
<span data-ttu-id="88b6c-126">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88b6c-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="88b6c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b6c-127">CommonParameters</span></span>
<span data-ttu-id="88b6c-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88b6c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b6c-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b6c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b6c-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b6c-130">INPUTS</span></span>

### <span data-ttu-id="88b6c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="88b6c-131">System.String</span></span>

### <span data-ttu-id="88b6c-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88b6c-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88b6c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88b6c-133">OUTPUTS</span></span>

### <span data-ttu-id="88b6c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="88b6c-134">System.String</span></span>

## <span data-ttu-id="88b6c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88b6c-135">NOTES</span></span>

## <span data-ttu-id="88b6c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88b6c-136">RELATED LINKS</span></span>

[<span data-ttu-id="88b6c-137">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88b6c-137">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="88b6c-138">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="88b6c-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="88b6c-139">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88b6c-139">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="88b6c-140">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="88b6c-140">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


