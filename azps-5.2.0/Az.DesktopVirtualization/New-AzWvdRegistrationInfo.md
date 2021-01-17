---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 2268135ebd1e1c504aae7462730d104e842f288f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332610"
---
# <span data-ttu-id="8f36a-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="8f36a-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="8f36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f36a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f36a-103">Virtuális windowsos asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f36a-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="8f36a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f36a-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f36a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f36a-105">DESCRIPTION</span></span>
<span data-ttu-id="8f36a-106">Virtuális windowsos asztali regisztrációs adatok létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f36a-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="8f36a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f36a-107">EXAMPLES</span></span>

### <span data-ttu-id="8f36a-108">1. példa: Virtuális asztali Windows regisztrációs jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="8f36a-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="8f36a-109">Ez a parancs létrehoz egy Windows virtuális asztali regisztrációs jogkivonatot egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="8f36a-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="8f36a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f36a-110">PARAMETERS</span></span>

### <span data-ttu-id="8f36a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f36a-111">-DefaultProfile</span></span>
<span data-ttu-id="8f36a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f36a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f36a-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="8f36a-113">-ExpirationTime</span></span>
<span data-ttu-id="8f36a-114">Lejárati idő</span><span class="sxs-lookup"><span data-stu-id="8f36a-114">Expiration Time</span></span>

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

### <span data-ttu-id="8f36a-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8f36a-115">-HostPoolName</span></span>
<span data-ttu-id="8f36a-116">Állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="8f36a-116">Host Pool Name</span></span>

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

### <span data-ttu-id="8f36a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f36a-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f36a-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8f36a-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8f36a-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f36a-119">-SubscriptionId</span></span>
<span data-ttu-id="8f36a-120">Előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="8f36a-120">Subscription Id</span></span>

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

### <span data-ttu-id="8f36a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f36a-121">-Confirm</span></span>
<span data-ttu-id="8f36a-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f36a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f36a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f36a-123">-WhatIf</span></span>
<span data-ttu-id="8f36a-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f36a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f36a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f36a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f36a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f36a-126">CommonParameters</span></span>
<span data-ttu-id="8f36a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f36a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f36a-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f36a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f36a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f36a-129">INPUTS</span></span>

## <span data-ttu-id="8f36a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f36a-130">OUTPUTS</span></span>

### <span data-ttu-id="8f36a-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="8f36a-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="8f36a-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f36a-132">NOTES</span></span>

<span data-ttu-id="8f36a-133">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8f36a-133">ALIASES</span></span>

## <span data-ttu-id="8f36a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f36a-134">RELATED LINKS</span></span>

