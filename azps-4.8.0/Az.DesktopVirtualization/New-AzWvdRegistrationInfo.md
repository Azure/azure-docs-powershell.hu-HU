---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185014"
---
# <span data-ttu-id="e7aca-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e7aca-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="e7aca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7aca-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aca-103">Windows virtuális asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7aca-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e7aca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7aca-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7aca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7aca-105">DESCRIPTION</span></span>
<span data-ttu-id="e7aca-106">Windows virtuális asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7aca-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e7aca-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e7aca-107">EXAMPLES</span></span>

### <span data-ttu-id="e7aca-108">Példa 1: Windows virtuális asztali regisztrációs jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="e7aca-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="e7aca-109">Ez a parancs létrehoz egy Windows virtuális asztali regisztrációs tokent egy állomás-készletben.</span><span class="sxs-lookup"><span data-stu-id="e7aca-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="e7aca-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7aca-110">PARAMETERS</span></span>

### <span data-ttu-id="e7aca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aca-111">-DefaultProfile</span></span>
<span data-ttu-id="e7aca-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7aca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="e7aca-113">-ExpirationTime</span></span>
<span data-ttu-id="e7aca-114">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="e7aca-114">Expiration Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e7aca-115">-HostPoolName</span></span>
<span data-ttu-id="e7aca-116">Állomáslista neve</span><span class="sxs-lookup"><span data-stu-id="e7aca-116">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aca-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7aca-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e7aca-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7aca-119">-SubscriptionId</span></span>
<span data-ttu-id="e7aca-120">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="e7aca-120">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7aca-121">-Confirm</span></span>
<span data-ttu-id="e7aca-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7aca-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7aca-123">-WhatIf</span></span>
<span data-ttu-id="e7aca-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7aca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7aca-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7aca-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aca-126">CommonParameters</span></span>
<span data-ttu-id="e7aca-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7aca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aca-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e7aca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aca-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7aca-129">INPUTS</span></span>

## <span data-ttu-id="e7aca-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7aca-130">OUTPUTS</span></span>

### <span data-ttu-id="e7aca-131">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e7aca-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="e7aca-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7aca-132">NOTES</span></span>

<span data-ttu-id="e7aca-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e7aca-133">ALIASES</span></span>

## <span data-ttu-id="e7aca-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7aca-134">RELATED LINKS</span></span>
