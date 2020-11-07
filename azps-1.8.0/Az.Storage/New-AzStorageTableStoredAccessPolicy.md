---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: e2e1f8952e0b785c5856585ad3e3371074194afd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668593"
---
# <span data-ttu-id="2fd37-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fd37-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="2fd37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2fd37-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd37-103">Egy, az Azure Storage-táblájához tárolt hozzáférési házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2fd37-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2fd37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2fd37-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fd37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2fd37-105">DESCRIPTION</span></span>
<span data-ttu-id="2fd37-106">A **New-AzStorageTableStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="2fd37-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2fd37-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2fd37-107">EXAMPLES</span></span>

### <span data-ttu-id="2fd37-108">Példa 1: tárolt hozzáférés-házirend létrehozása táblázatban</span><span class="sxs-lookup"><span data-stu-id="2fd37-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="2fd37-109">A parancs létrehoz egy Policy02 nevű Access-házirendet a táblanév nevű tárterület táblában.</span><span class="sxs-lookup"><span data-stu-id="2fd37-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="2fd37-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2fd37-110">PARAMETERS</span></span>

### <span data-ttu-id="2fd37-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2fd37-111">-Context</span></span>
<span data-ttu-id="2fd37-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fd37-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2fd37-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2fd37-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2fd37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd37-114">-DefaultProfile</span></span>
<span data-ttu-id="2fd37-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2fd37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd37-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2fd37-116">-ExpiryTime</span></span>
<span data-ttu-id="2fd37-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="2fd37-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="2fd37-118">– Engedély</span><span class="sxs-lookup"><span data-stu-id="2fd37-118">-Permission</span></span>
<span data-ttu-id="2fd37-119">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="2fd37-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="2fd37-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="2fd37-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="2fd37-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="2fd37-121">-Policy</span></span>
<span data-ttu-id="2fd37-122">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fd37-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="2fd37-123">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="2fd37-123">-StartTime</span></span>
<span data-ttu-id="2fd37-124">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="2fd37-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="2fd37-125">-Table</span><span class="sxs-lookup"><span data-stu-id="2fd37-125">-Table</span></span>
<span data-ttu-id="2fd37-126">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2fd37-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="2fd37-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd37-127">CommonParameters</span></span>
<span data-ttu-id="2fd37-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2fd37-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd37-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd37-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd37-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fd37-130">INPUTS</span></span>

### <span data-ttu-id="2fd37-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2fd37-131">System.String</span></span>

### <span data-ttu-id="2fd37-132">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fd37-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2fd37-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fd37-133">OUTPUTS</span></span>

### <span data-ttu-id="2fd37-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2fd37-134">System.String</span></span>

## <span data-ttu-id="2fd37-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2fd37-135">NOTES</span></span>

## <span data-ttu-id="2fd37-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fd37-136">RELATED LINKS</span></span>

[<span data-ttu-id="2fd37-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fd37-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2fd37-138">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fd37-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2fd37-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fd37-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2fd37-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2fd37-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


