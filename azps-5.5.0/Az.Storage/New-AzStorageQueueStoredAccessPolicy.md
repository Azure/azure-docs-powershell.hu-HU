---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207783"
---
# <span data-ttu-id="62703-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62703-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="62703-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62703-102">SYNOPSIS</span></span>
<span data-ttu-id="62703-103">Tárolt hozzáférési házirendet hoz létre egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="62703-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="62703-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62703-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62703-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62703-105">DESCRIPTION</span></span>
<span data-ttu-id="62703-106">A **New-AzStorageQueueStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="62703-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="62703-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62703-107">EXAMPLES</span></span>

### <span data-ttu-id="62703-108">1. példa: Tárolt hozzáférési házirend létrehozása tár várólistán</span><span class="sxs-lookup"><span data-stu-id="62703-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="62703-109">Ez a parancs létrehoz egy Policy01 nevű hozzáférési házirendet a MyQueue nevű tár várólistán.</span><span class="sxs-lookup"><span data-stu-id="62703-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="62703-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62703-110">PARAMETERS</span></span>

### <span data-ttu-id="62703-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="62703-111">-Context</span></span>
<span data-ttu-id="62703-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62703-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="62703-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="62703-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="62703-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62703-114">-DefaultProfile</span></span>
<span data-ttu-id="62703-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62703-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62703-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="62703-116">-ExpiryTime</span></span>
<span data-ttu-id="62703-117">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="62703-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="62703-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="62703-118">-Permission</span></span>
<span data-ttu-id="62703-119">A tárterület-várólistához való hozzáférésre vonatkozó engedélyeket adja meg a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="62703-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="62703-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="62703-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="62703-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="62703-121">-Policy</span></span>
<span data-ttu-id="62703-122">Megadja a tárolt hozzáférési házirend nevét.</span><span class="sxs-lookup"><span data-stu-id="62703-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="62703-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="62703-123">-Queue</span></span>
<span data-ttu-id="62703-124">Az Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62703-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="62703-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="62703-125">-StartTime</span></span>
<span data-ttu-id="62703-126">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="62703-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="62703-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62703-127">CommonParameters</span></span>
<span data-ttu-id="62703-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62703-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62703-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62703-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62703-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62703-130">INPUTS</span></span>

### <span data-ttu-id="62703-131">System.String</span><span class="sxs-lookup"><span data-stu-id="62703-131">System.String</span></span>

### <span data-ttu-id="62703-132">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="62703-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="62703-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62703-133">OUTPUTS</span></span>

### <span data-ttu-id="62703-134">System.String</span><span class="sxs-lookup"><span data-stu-id="62703-134">System.String</span></span>

## <span data-ttu-id="62703-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62703-135">NOTES</span></span>

## <span data-ttu-id="62703-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62703-136">RELATED LINKS</span></span>

[<span data-ttu-id="62703-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62703-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="62703-138">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="62703-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="62703-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62703-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="62703-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62703-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


