---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 0ec79b50d47a86b23e7c55e7277fe567ba46b9d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672501"
---
# <span data-ttu-id="11d45-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11d45-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="11d45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11d45-102">SYNOPSIS</span></span>
<span data-ttu-id="11d45-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure Storage table.</span><span class="sxs-lookup"><span data-stu-id="11d45-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11d45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11d45-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11d45-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="11d45-105">DESCRIPTION</span></span>
<span data-ttu-id="11d45-106">A **Get-AzureStorageTableStoredAccessPolicy** parancsmag felsorolja az Azure Storage Tables tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="11d45-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="11d45-107">Példák</span><span class="sxs-lookup"><span data-stu-id="11d45-107">EXAMPLES</span></span>

### <span data-ttu-id="11d45-108">Példa 1: tárolt hozzáférés-házirend beszerzése tárterület-táblában</span><span class="sxs-lookup"><span data-stu-id="11d45-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="11d45-109">Ez a parancs a Policy50 nevű Access-házirendet a Table02 nevű tárolási táblában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11d45-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="11d45-110">2. példa: az összes tárolt Access-házirend beolvasása egy tárterület-táblában</span><span class="sxs-lookup"><span data-stu-id="11d45-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="11d45-111">Ez a parancs a Table02 nevű táblázat minden hozzáférési házirendjét bekapja.</span><span class="sxs-lookup"><span data-stu-id="11d45-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="11d45-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11d45-112">PARAMETERS</span></span>

### <span data-ttu-id="11d45-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="11d45-113">-Context</span></span>
<span data-ttu-id="11d45-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11d45-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="11d45-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="11d45-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="11d45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d45-116">-DefaultProfile</span></span>
<span data-ttu-id="11d45-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11d45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d45-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="11d45-118">-Policy</span></span>
<span data-ttu-id="11d45-119">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="11d45-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11d45-120">-Table</span><span class="sxs-lookup"><span data-stu-id="11d45-120">-Table</span></span>
<span data-ttu-id="11d45-121">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11d45-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="11d45-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d45-122">CommonParameters</span></span>
<span data-ttu-id="11d45-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11d45-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d45-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d45-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d45-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11d45-125">INPUTS</span></span>

### <span data-ttu-id="11d45-126">System. String</span><span class="sxs-lookup"><span data-stu-id="11d45-126">System.String</span></span>

### <span data-ttu-id="11d45-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="11d45-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="11d45-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11d45-128">OUTPUTS</span></span>

### <span data-ttu-id="11d45-129">Microsoft. WindowsAzure. Storage. table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="11d45-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="11d45-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11d45-130">NOTES</span></span>

## <span data-ttu-id="11d45-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11d45-131">RELATED LINKS</span></span>

[<span data-ttu-id="11d45-132">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11d45-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="11d45-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11d45-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="11d45-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="11d45-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="11d45-135">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="11d45-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


