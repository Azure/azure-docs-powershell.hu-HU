---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207806"
---
# <span data-ttu-id="6c1a6-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1a6-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="6c1a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1a6-103">Egy Azure-tárterület-várólistán tárolt hozzáférési házirendet vagy házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="6c1a6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c1a6-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c1a6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c1a6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c1a6-106">A **Get-AzStorageQueueStoredAccessPolicy** parancsmag felsorolja egy Azure-tár várólistán tárolt hozzáférési házirendet vagy házirendeket.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="6c1a6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c1a6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c1a6-108">1. példa: Tárolt hozzáférési házirend kérése a várólistán</span><span class="sxs-lookup"><span data-stu-id="6c1a6-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="6c1a6-109">Ez a parancs a Házirend12 hozzáférési házirendet a MyQueue nevű társorba kapja.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="6c1a6-110">2. példa: Az összes tárolt hozzáférési házirend behozása a várólistára</span><span class="sxs-lookup"><span data-stu-id="6c1a6-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="6c1a6-111">Ez a parancs az összes tárolt hozzáférési házirendet a MyQueue nevű várólistába kapja.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="6c1a6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c1a6-112">PARAMETERS</span></span>

### <span data-ttu-id="6c1a6-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6c1a6-113">-Context</span></span>
<span data-ttu-id="6c1a6-114">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6c1a6-115">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6c1a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1a6-116">-DefaultProfile</span></span>
<span data-ttu-id="6c1a6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c1a6-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="6c1a6-118">-Policy</span></span>
<span data-ttu-id="6c1a6-119">Egy tárolt hozzáférési házirendet ad meg, amely tartalmazza a Megosztott hozzáférés-aláírás (SAS) jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="6c1a6-120">-Queue</span><span class="sxs-lookup"><span data-stu-id="6c1a6-120">-Queue</span></span>
<span data-ttu-id="6c1a6-121">Az Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="6c1a6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1a6-122">CommonParameters</span></span>
<span data-ttu-id="6c1a6-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c1a6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1a6-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1a6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1a6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c1a6-125">INPUTS</span></span>

### <span data-ttu-id="6c1a6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6c1a6-126">System.String</span></span>

### <span data-ttu-id="6c1a6-127">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c1a6-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6c1a6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c1a6-128">OUTPUTS</span></span>

### <span data-ttu-id="6c1a6-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="6c1a6-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="6c1a6-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c1a6-130">NOTES</span></span>

## <span data-ttu-id="6c1a6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c1a6-131">RELATED LINKS</span></span>

[<span data-ttu-id="6c1a6-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1a6-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6c1a6-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1a6-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6c1a6-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1a6-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="6c1a6-135">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="6c1a6-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


