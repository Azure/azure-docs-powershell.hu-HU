---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9c740dec8cc2e3f3666d00c12def3eefb7cafce9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839719"
---
# <span data-ttu-id="e9e20-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e20-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e9e20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e9e20-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e20-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="e9e20-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="e9e20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e9e20-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e9e20-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e20-106">A **Get-AzStorageQueueStoredAccessPolicy** parancsmag felsorolja az Azure-tárterületek várólistájának tárolt elérési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="e9e20-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="e9e20-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e9e20-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e20-108">1. példa: tárolt hozzáférési házirend beszerzése a várólistában</span><span class="sxs-lookup"><span data-stu-id="e9e20-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="e9e20-109">Ez a parancs a Policy12 nevű Access-házirendet a MyQueue nevű tárolási várólistában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e9e20-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="e9e20-110">2. példa: az összes tárolt Access-házirend beolvasása a várólistán</span><span class="sxs-lookup"><span data-stu-id="e9e20-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="e9e20-111">Ez a parancs a MyQueue nevű várólistában minden tárolt Access-házirendet beolvas.</span><span class="sxs-lookup"><span data-stu-id="e9e20-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="e9e20-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e9e20-112">PARAMETERS</span></span>

### <span data-ttu-id="e9e20-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e9e20-113">-Context</span></span>
<span data-ttu-id="e9e20-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9e20-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e9e20-115">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e9e20-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e9e20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e20-116">-DefaultProfile</span></span>
<span data-ttu-id="e9e20-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9e20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9e20-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e9e20-118">-Policy</span></span>
<span data-ttu-id="e9e20-119">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="e9e20-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="e9e20-120">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="e9e20-120">-Queue</span></span>
<span data-ttu-id="e9e20-121">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9e20-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="e9e20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e20-122">CommonParameters</span></span>
<span data-ttu-id="e9e20-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e9e20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e20-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9e20-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e20-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9e20-125">INPUTS</span></span>

### <span data-ttu-id="e9e20-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e9e20-126">System.String</span></span>

### <span data-ttu-id="e9e20-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9e20-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9e20-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9e20-128">OUTPUTS</span></span>

### <span data-ttu-id="e9e20-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="e9e20-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="e9e20-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e9e20-130">NOTES</span></span>

## <span data-ttu-id="e9e20-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9e20-131">RELATED LINKS</span></span>

[<span data-ttu-id="e9e20-132">Új – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e20-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e9e20-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e20-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e9e20-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9e20-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e9e20-135">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9e20-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


