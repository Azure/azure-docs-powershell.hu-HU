---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479433"
---
# <span data-ttu-id="d1f33-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1f33-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d1f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f33-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f33-103">Tárolt hozzáférési házirendet hoz létre egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="d1f33-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="d1f33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d1f33-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1f33-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d1f33-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f33-106">A **New-AzStorageQueueStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="d1f33-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="d1f33-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d1f33-107">EXAMPLES</span></span>

### <span data-ttu-id="d1f33-108">1. példa: Tárolt hozzáférési házirend létrehozása tár várólistán</span><span class="sxs-lookup"><span data-stu-id="d1f33-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="d1f33-109">Ez a parancs létrehoz egy Policy01 nevű hozzáférési házirendet a MyQueue nevű tár várólistán.</span><span class="sxs-lookup"><span data-stu-id="d1f33-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="d1f33-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f33-110">PARAMETERS</span></span>

### <span data-ttu-id="d1f33-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d1f33-111">-Context</span></span>
<span data-ttu-id="d1f33-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1f33-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d1f33-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d1f33-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d1f33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f33-114">-DefaultProfile</span></span>
<span data-ttu-id="d1f33-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1f33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f33-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d1f33-116">-ExpiryTime</span></span>
<span data-ttu-id="d1f33-117">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="d1f33-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="d1f33-118">-Engedély</span><span class="sxs-lookup"><span data-stu-id="d1f33-118">-Permission</span></span>
<span data-ttu-id="d1f33-119">Engedélyeket ad meg a tárterület-várólistához való hozzáféréshez a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="d1f33-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="d1f33-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="d1f33-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d1f33-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="d1f33-121">-Policy</span></span>
<span data-ttu-id="d1f33-122">Megadja a tárolt hozzáférési házirend nevét.</span><span class="sxs-lookup"><span data-stu-id="d1f33-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="d1f33-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="d1f33-123">-Queue</span></span>
<span data-ttu-id="d1f33-124">Az Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1f33-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d1f33-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d1f33-125">-StartTime</span></span>
<span data-ttu-id="d1f33-126">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="d1f33-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="d1f33-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f33-127">CommonParameters</span></span>
<span data-ttu-id="d1f33-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f33-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f33-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1f33-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f33-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1f33-130">INPUTS</span></span>

### <span data-ttu-id="d1f33-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d1f33-131">System.String</span></span>

### <span data-ttu-id="d1f33-132">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1f33-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1f33-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1f33-133">OUTPUTS</span></span>

### <span data-ttu-id="d1f33-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d1f33-134">System.String</span></span>

## <span data-ttu-id="d1f33-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d1f33-135">NOTES</span></span>

## <span data-ttu-id="d1f33-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1f33-136">RELATED LINKS</span></span>

[<span data-ttu-id="d1f33-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1f33-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d1f33-138">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="d1f33-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d1f33-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1f33-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d1f33-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d1f33-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


