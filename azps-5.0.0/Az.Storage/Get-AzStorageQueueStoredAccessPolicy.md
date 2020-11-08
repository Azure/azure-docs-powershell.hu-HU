---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186341"
---
# <span data-ttu-id="a8779-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8779-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a8779-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8779-102">SYNOPSIS</span></span>
<span data-ttu-id="a8779-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="a8779-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="a8779-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8779-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8779-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8779-105">DESCRIPTION</span></span>
<span data-ttu-id="a8779-106">A **Get-AzStorageQueueStoredAccessPolicy** parancsmag felsorolja az Azure-tárterületek várólistájának tárolt elérési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="a8779-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="a8779-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8779-107">EXAMPLES</span></span>

### <span data-ttu-id="a8779-108">1. példa: tárolt hozzáférési házirend beszerzése a várólistában</span><span class="sxs-lookup"><span data-stu-id="a8779-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="a8779-109">Ez a parancs a Policy12 nevű Access-házirendet a MyQueue nevű tárolási várólistában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a8779-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="a8779-110">2. példa: az összes tárolt Access-házirend beolvasása a várólistán</span><span class="sxs-lookup"><span data-stu-id="a8779-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="a8779-111">Ez a parancs a MyQueue nevű várólistában minden tárolt Access-házirendet beolvas.</span><span class="sxs-lookup"><span data-stu-id="a8779-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="a8779-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8779-112">PARAMETERS</span></span>

### <span data-ttu-id="a8779-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a8779-113">-Context</span></span>
<span data-ttu-id="a8779-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8779-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a8779-115">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a8779-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a8779-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8779-116">-DefaultProfile</span></span>
<span data-ttu-id="a8779-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8779-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8779-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a8779-118">-Policy</span></span>
<span data-ttu-id="a8779-119">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="a8779-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a8779-120">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="a8779-120">-Queue</span></span>
<span data-ttu-id="a8779-121">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8779-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a8779-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8779-122">CommonParameters</span></span>
<span data-ttu-id="a8779-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8779-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8779-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8779-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8779-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8779-125">INPUTS</span></span>

### <span data-ttu-id="a8779-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a8779-126">System.String</span></span>

### <span data-ttu-id="a8779-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8779-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a8779-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8779-128">OUTPUTS</span></span>

### <span data-ttu-id="a8779-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="a8779-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="a8779-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8779-130">NOTES</span></span>

## <span data-ttu-id="a8779-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8779-131">RELATED LINKS</span></span>

[<span data-ttu-id="a8779-132">Új – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8779-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a8779-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8779-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a8779-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a8779-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a8779-135">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a8779-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

