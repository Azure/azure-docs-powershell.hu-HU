---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940753"
---
# <span data-ttu-id="b61ad-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b61ad-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b61ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b61ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b61ad-103">Egy Azure-tárolótáblához tárolt hozzáférési házirendet vagy házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="b61ad-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b61ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b61ad-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61ad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b61ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b61ad-106">A **Get-AzStorageTableStoredAccessPolicy** parancsmag felsorolja az Azure-tárolótáblák tárolt hozzáférési házirendeit vagy házirendeit.</span><span class="sxs-lookup"><span data-stu-id="b61ad-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b61ad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b61ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b61ad-108">1. példa: Tárolt hozzáférési házirend lekérte egy tárolótáblában</span><span class="sxs-lookup"><span data-stu-id="b61ad-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b61ad-109">Ez a parancs a Policy50 nevű hozzáférési házirendet a Table02 nevű tárolótáblába kapja.</span><span class="sxs-lookup"><span data-stu-id="b61ad-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b61ad-110">2. példa: Az összes tárolt hozzáférési házirend lekérte egy tárolótáblába</span><span class="sxs-lookup"><span data-stu-id="b61ad-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b61ad-111">Ez a parancs a Table02 nevű táblában található összes hozzáférési házirendet beveszi.</span><span class="sxs-lookup"><span data-stu-id="b61ad-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b61ad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b61ad-112">PARAMETERS</span></span>

### <span data-ttu-id="b61ad-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b61ad-113">-Context</span></span>
<span data-ttu-id="b61ad-114">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b61ad-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b61ad-115">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b61ad-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b61ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61ad-116">-DefaultProfile</span></span>
<span data-ttu-id="b61ad-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b61ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b61ad-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b61ad-118">-Policy</span></span>
<span data-ttu-id="b61ad-119">Egy tárolt hozzáférési házirendet ad meg, amely tartalmazza a Megosztott hozzáférés-aláírás (SAS) jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="b61ad-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b61ad-120">-Table</span><span class="sxs-lookup"><span data-stu-id="b61ad-120">-Table</span></span>
<span data-ttu-id="b61ad-121">Az Azure-tártábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b61ad-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b61ad-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61ad-122">CommonParameters</span></span>
<span data-ttu-id="b61ad-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61ad-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61ad-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61ad-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61ad-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b61ad-125">INPUTS</span></span>

### <span data-ttu-id="b61ad-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b61ad-126">System.String</span></span>

### <span data-ttu-id="b61ad-127">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b61ad-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b61ad-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b61ad-128">OUTPUTS</span></span>

### <span data-ttu-id="b61ad-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="b61ad-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="b61ad-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b61ad-130">NOTES</span></span>

## <span data-ttu-id="b61ad-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b61ad-131">RELATED LINKS</span></span>

[<span data-ttu-id="b61ad-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b61ad-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b61ad-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b61ad-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b61ad-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b61ad-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b61ad-135">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="b61ad-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


