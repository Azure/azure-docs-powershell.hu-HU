---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9ef4be8331c1de38789d25903db9e98f4e2d8cd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848577"
---
# <span data-ttu-id="dafcb-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dafcb-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="dafcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dafcb-102">SYNOPSIS</span></span>
<span data-ttu-id="dafcb-103">Beolvassa a tárolt hozzáférési házirendet vagy házirendet egy Azure-tárterület várólistájához.</span><span class="sxs-lookup"><span data-stu-id="dafcb-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dafcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dafcb-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dafcb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dafcb-105">DESCRIPTION</span></span>
<span data-ttu-id="dafcb-106">A **Get-AzureStorageQueueStoredAccessPolicy** parancsmag felsorolja az Azure-tárterületek várólistájának tárolt elérési házirendjét vagy házirendjeit.</span><span class="sxs-lookup"><span data-stu-id="dafcb-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="dafcb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dafcb-107">EXAMPLES</span></span>

### <span data-ttu-id="dafcb-108">1. példa: tárolt hozzáférési házirend beszerzése a várólistában</span><span class="sxs-lookup"><span data-stu-id="dafcb-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="dafcb-109">Ez a parancs a Policy12 nevű Access-házirendet a MyQueue nevű tárolási várólistában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dafcb-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="dafcb-110">2. példa: az összes tárolt Access-házirend beolvasása a várólistán</span><span class="sxs-lookup"><span data-stu-id="dafcb-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="dafcb-111">Ez a parancs a MyQueue nevű várólistában minden tárolt Access-házirendet beolvas.</span><span class="sxs-lookup"><span data-stu-id="dafcb-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="dafcb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dafcb-112">PARAMETERS</span></span>

### <span data-ttu-id="dafcb-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dafcb-113">-Context</span></span>
<span data-ttu-id="dafcb-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dafcb-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dafcb-115">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dafcb-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dafcb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafcb-116">-DefaultProfile</span></span>
<span data-ttu-id="dafcb-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dafcb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dafcb-118">-Házirend</span><span class="sxs-lookup"><span data-stu-id="dafcb-118">-Policy</span></span>
<span data-ttu-id="dafcb-119">A tárolt Access-házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="dafcb-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="dafcb-120">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="dafcb-120">-Queue</span></span>
<span data-ttu-id="dafcb-121">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="dafcb-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="dafcb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafcb-122">CommonParameters</span></span>
<span data-ttu-id="dafcb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dafcb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafcb-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafcb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafcb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafcb-125">INPUTS</span></span>

### <span data-ttu-id="dafcb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dafcb-126">System.String</span></span>

### <span data-ttu-id="dafcb-127">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dafcb-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dafcb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafcb-128">OUTPUTS</span></span>

### <span data-ttu-id="dafcb-129">Microsoft. WindowsAzure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="dafcb-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="dafcb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dafcb-130">NOTES</span></span>

## <span data-ttu-id="dafcb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dafcb-131">RELATED LINKS</span></span>

[<span data-ttu-id="dafcb-132">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dafcb-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="dafcb-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dafcb-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="dafcb-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dafcb-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="dafcb-135">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dafcb-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

