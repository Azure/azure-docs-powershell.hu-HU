---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156427"
---
# <span data-ttu-id="4e4c5-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="4e4c5-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="4e4c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4c5-103">Az előfizetéshez konfigurált biztonsági partnerek lekérte</span><span class="sxs-lookup"><span data-stu-id="4e4c5-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="4e4c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4e4c5-104">SYNTAX</span></span>

### <span data-ttu-id="4e4c5-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e4c5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e4c5-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4e4c5-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e4c5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e4c5-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e4c5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4e4c5-108">DESCRIPTION</span></span>
<span data-ttu-id="4e4c5-109">Az előfizetéshez konfigurált biztonsági névjegyeket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="4e4c5-110">A biztonsági partner értesítéseket kaphat az előfizetésen bekövetkező biztonsági riasztásokkal kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="4e4c5-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4e4c5-111">EXAMPLES</span></span>

### <span data-ttu-id="4e4c5-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="4e4c5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="4e4c5-113">Az előfizetéshez konfigurált biztonsági partnerek lekérte</span><span class="sxs-lookup"><span data-stu-id="4e4c5-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="4e4c5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e4c5-114">PARAMETERS</span></span>

### <span data-ttu-id="4e4c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4c5-115">-DefaultProfile</span></span>
<span data-ttu-id="4e4c5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e4c5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4e4c5-117">-Name</span></span>
<span data-ttu-id="4e4c5-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4c5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e4c5-119">-ResourceId</span></span>
<span data-ttu-id="4e4c5-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e4c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4c5-121">CommonParameters</span></span>
<span data-ttu-id="4e4c5-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4c5-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e4c5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4c5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e4c5-124">INPUTS</span></span>

### <span data-ttu-id="4e4c5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4e4c5-125">System.String</span></span>

## <span data-ttu-id="4e4c5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e4c5-126">OUTPUTS</span></span>

### <span data-ttu-id="4e4c5-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="4e4c5-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="4e4c5-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4e4c5-128">NOTES</span></span>

## <span data-ttu-id="4e4c5-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e4c5-129">RELATED LINKS</span></span>
