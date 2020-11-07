---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: c079b65dc0a37ea07815e2e3b47799b9a194f4e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843045"
---
# <span data-ttu-id="5a85e-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a85e-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5a85e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a85e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a85e-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure Storage table.</span><span class="sxs-lookup"><span data-stu-id="5a85e-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="5a85e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a85e-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a85e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a85e-105">DESCRIPTION</span></span>
<span data-ttu-id="5a85e-106">A **Get-AzStorageTableStoredAccessPolicy** parancsmag felsorolja az Azure Storage Tables tárolt hozzáférési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="5a85e-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="5a85e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5a85e-107">EXAMPLES</span></span>

### <span data-ttu-id="5a85e-108">Példa 1: tárolt hozzáférés-házirend beszerzése tárterület-táblában</span><span class="sxs-lookup"><span data-stu-id="5a85e-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="5a85e-109">Ez a parancs a Policy50 nevű Access-házirendet a Table02 nevű tárolási táblában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a85e-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="5a85e-110">2. példa: az összes tárolt Access-házirend beolvasása egy tárterület-táblában</span><span class="sxs-lookup"><span data-stu-id="5a85e-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="5a85e-111">Ez a parancs a Table02 nevű táblázat minden hozzáférési házirendjét bekapja.</span><span class="sxs-lookup"><span data-stu-id="5a85e-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="5a85e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a85e-112">PARAMETERS</span></span>

### <span data-ttu-id="5a85e-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5a85e-113">-Context</span></span>
<span data-ttu-id="5a85e-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a85e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5a85e-115">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5a85e-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5a85e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a85e-116">-DefaultProfile</span></span>
<span data-ttu-id="5a85e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a85e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a85e-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="5a85e-118">-Policy</span></span>
<span data-ttu-id="5a85e-119">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="5a85e-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="5a85e-120">-Table</span><span class="sxs-lookup"><span data-stu-id="5a85e-120">-Table</span></span>
<span data-ttu-id="5a85e-121">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a85e-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="5a85e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a85e-122">CommonParameters</span></span>
<span data-ttu-id="5a85e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a85e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a85e-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a85e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a85e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a85e-125">INPUTS</span></span>

### <span data-ttu-id="5a85e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5a85e-126">System.String</span></span>

### <span data-ttu-id="5a85e-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a85e-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5a85e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a85e-128">OUTPUTS</span></span>

### <span data-ttu-id="5a85e-129">Microsoft. WindowsAz. Storage. table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="5a85e-129">Microsoft.WindowsAz.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="5a85e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a85e-130">NOTES</span></span>

## <span data-ttu-id="5a85e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a85e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a85e-132">Új – AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a85e-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5a85e-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a85e-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5a85e-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a85e-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5a85e-135">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="5a85e-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


