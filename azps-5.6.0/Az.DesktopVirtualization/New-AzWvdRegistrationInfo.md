---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 7e633d2ba607132de6dbdfc262642659cc5e4c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925666"
---
# <span data-ttu-id="46528-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="46528-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="46528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46528-102">SYNOPSIS</span></span>
<span data-ttu-id="46528-103">Virtuális windowsos asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="46528-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="46528-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="46528-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46528-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="46528-105">DESCRIPTION</span></span>
<span data-ttu-id="46528-106">Virtuális windowsos asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="46528-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="46528-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="46528-107">EXAMPLES</span></span>

### <span data-ttu-id="46528-108">1. példa: Virtuális asztali Windows regisztrációs jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="46528-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="46528-109">Ez a parancs létrehoz egy Windows virtuális asztali regisztrációs jogkivonatot egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="46528-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="46528-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46528-110">PARAMETERS</span></span>

### <span data-ttu-id="46528-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46528-111">-DefaultProfile</span></span>
<span data-ttu-id="46528-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46528-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46528-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="46528-113">-ExpirationTime</span></span>
<span data-ttu-id="46528-114">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="46528-114">Expiration Time</span></span>

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

### <span data-ttu-id="46528-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="46528-115">-HostPoolName</span></span>
<span data-ttu-id="46528-116">Állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="46528-116">Host Pool Name</span></span>

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

### <span data-ttu-id="46528-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46528-117">-ResourceGroupName</span></span>
<span data-ttu-id="46528-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="46528-118">Resource Group Name</span></span>

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

### <span data-ttu-id="46528-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46528-119">-SubscriptionId</span></span>
<span data-ttu-id="46528-120">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="46528-120">Subscription Id</span></span>

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

### <span data-ttu-id="46528-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46528-121">-Confirm</span></span>
<span data-ttu-id="46528-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="46528-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46528-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46528-123">-WhatIf</span></span>
<span data-ttu-id="46528-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="46528-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46528-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46528-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46528-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46528-126">CommonParameters</span></span>
<span data-ttu-id="46528-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46528-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46528-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46528-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46528-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46528-129">INPUTS</span></span>

## <span data-ttu-id="46528-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46528-130">OUTPUTS</span></span>

### <span data-ttu-id="46528-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="46528-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="46528-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="46528-132">NOTES</span></span>

<span data-ttu-id="46528-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="46528-133">ALIASES</span></span>

## <span data-ttu-id="46528-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46528-134">RELATED LINKS</span></span>

