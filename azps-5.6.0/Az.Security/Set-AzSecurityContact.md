---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 8cd5adee5e8b992cf709b76996a70760f3fd90a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936025"
---
# <span data-ttu-id="0a580-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="0a580-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="0a580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a580-102">SYNOPSIS</span></span>
<span data-ttu-id="0a580-103">Frissíti egy előfizetés biztonsági kapcsolattartóját.</span><span class="sxs-lookup"><span data-stu-id="0a580-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0a580-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a580-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a580-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a580-105">DESCRIPTION</span></span>
<span data-ttu-id="0a580-106">Frissíti egy előfizetés biztonsági kapcsolattartóját.</span><span class="sxs-lookup"><span data-stu-id="0a580-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0a580-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a580-107">EXAMPLES</span></span>

### <span data-ttu-id="0a580-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0a580-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="0a580-109">Frissíti egy előfizetés biztonsági kapcsolattartóját.</span><span class="sxs-lookup"><span data-stu-id="0a580-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="0a580-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a580-110">PARAMETERS</span></span>

### <span data-ttu-id="0a580-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="0a580-111">-AlertAdmin</span></span>
<span data-ttu-id="0a580-112">Riasztások rendszergazdáknak.</span><span class="sxs-lookup"><span data-stu-id="0a580-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a580-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a580-113">-DefaultProfile</span></span>
<span data-ttu-id="0a580-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a580-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a580-115">-Email</span><span class="sxs-lookup"><span data-stu-id="0a580-115">-Email</span></span>
<span data-ttu-id="0a580-116">E-mail.</span><span class="sxs-lookup"><span data-stu-id="0a580-116">E-Mail.</span></span>

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

### <span data-ttu-id="0a580-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0a580-117">-Name</span></span>
<span data-ttu-id="0a580-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0a580-118">Resource name.</span></span>

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

### <span data-ttu-id="0a580-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="0a580-119">-NotifyOnAlert</span></span>
<span data-ttu-id="0a580-120">Értesítési értesítések.</span><span class="sxs-lookup"><span data-stu-id="0a580-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a580-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="0a580-121">-Phone</span></span>
<span data-ttu-id="0a580-122">Telefon 2010.</span><span class="sxs-lookup"><span data-stu-id="0a580-122">Phone.</span></span>

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

### <span data-ttu-id="0a580-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a580-123">-Confirm</span></span>
<span data-ttu-id="0a580-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0a580-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a580-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a580-125">-WhatIf</span></span>
<span data-ttu-id="0a580-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0a580-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a580-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0a580-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a580-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a580-128">CommonParameters</span></span>
<span data-ttu-id="0a580-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a580-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a580-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a580-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a580-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a580-131">INPUTS</span></span>

### <span data-ttu-id="0a580-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="0a580-132">None</span></span>

## <span data-ttu-id="0a580-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a580-133">OUTPUTS</span></span>

### <span data-ttu-id="0a580-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="0a580-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="0a580-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a580-135">NOTES</span></span>

## <span data-ttu-id="0a580-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a580-136">RELATED LINKS</span></span>
