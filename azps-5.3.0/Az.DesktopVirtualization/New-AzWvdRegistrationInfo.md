---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387265"
---
# <span data-ttu-id="e300e-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e300e-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="e300e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e300e-102">SYNOPSIS</span></span>
<span data-ttu-id="e300e-103">Virtuális windowsos asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="e300e-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e300e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e300e-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e300e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e300e-105">DESCRIPTION</span></span>
<span data-ttu-id="e300e-106">Virtuális windowsos asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="e300e-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="e300e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e300e-107">EXAMPLES</span></span>

### <span data-ttu-id="e300e-108">1. példa: Virtuális asztali Windows regisztrációs jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="e300e-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="e300e-109">Ez a parancs létrehoz egy Windows virtuális asztali regisztrációs jogkivonatot egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="e300e-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="e300e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e300e-110">PARAMETERS</span></span>

### <span data-ttu-id="e300e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e300e-111">-DefaultProfile</span></span>
<span data-ttu-id="e300e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e300e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e300e-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="e300e-113">-ExpirationTime</span></span>
<span data-ttu-id="e300e-114">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="e300e-114">Expiration Time</span></span>

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

### <span data-ttu-id="e300e-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e300e-115">-HostPoolName</span></span>
<span data-ttu-id="e300e-116">Állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="e300e-116">Host Pool Name</span></span>

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

### <span data-ttu-id="e300e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e300e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e300e-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e300e-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e300e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e300e-119">-SubscriptionId</span></span>
<span data-ttu-id="e300e-120">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="e300e-120">Subscription Id</span></span>

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

### <span data-ttu-id="e300e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e300e-121">-Confirm</span></span>
<span data-ttu-id="e300e-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e300e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e300e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e300e-123">-WhatIf</span></span>
<span data-ttu-id="e300e-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e300e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e300e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e300e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e300e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e300e-126">CommonParameters</span></span>
<span data-ttu-id="e300e-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e300e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e300e-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e300e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e300e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e300e-129">INPUTS</span></span>

## <span data-ttu-id="e300e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e300e-130">OUTPUTS</span></span>

### <span data-ttu-id="e300e-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="e300e-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="e300e-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e300e-132">NOTES</span></span>

<span data-ttu-id="e300e-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e300e-133">ALIASES</span></span>

## <span data-ttu-id="e300e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e300e-134">RELATED LINKS</span></span>

