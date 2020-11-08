---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186047"
---
# <span data-ttu-id="29e37-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="29e37-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="29e37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29e37-102">SYNOPSIS</span></span>
<span data-ttu-id="29e37-103">Egy névtérhez tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="29e37-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="29e37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29e37-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29e37-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29e37-105">DESCRIPTION</span></span>
<span data-ttu-id="29e37-106">New-AzNotificationHubNamespaceKey parancsmag újragenerálja a névtér-engedélyezési szabály elsődleges kulcsát/másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="29e37-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="29e37-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29e37-107">EXAMPLES</span></span>

### <span data-ttu-id="29e37-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29e37-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="29e37-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="29e37-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="29e37-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29e37-110">PARAMETERS</span></span>

### <span data-ttu-id="29e37-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="29e37-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e37-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e37-112">-DefaultProfile</span></span>
<span data-ttu-id="29e37-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="29e37-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29e37-114">-Force</span><span class="sxs-lookup"><span data-stu-id="29e37-114">-Force</span></span>
<span data-ttu-id="29e37-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29e37-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="29e37-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="29e37-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e37-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="29e37-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e37-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="29e37-118">-ResourceGroup</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e37-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29e37-119">-Confirm</span></span>
<span data-ttu-id="29e37-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29e37-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29e37-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e37-121">-WhatIf</span></span>
<span data-ttu-id="29e37-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29e37-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29e37-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29e37-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29e37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e37-124">CommonParameters</span></span>
<span data-ttu-id="29e37-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29e37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e37-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e37-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e37-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29e37-127">INPUTS</span></span>

### <span data-ttu-id="29e37-128">System. String</span><span class="sxs-lookup"><span data-stu-id="29e37-128">System.String</span></span>

## <span data-ttu-id="29e37-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29e37-129">OUTPUTS</span></span>

### <span data-ttu-id="29e37-130">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="29e37-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="29e37-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29e37-131">NOTES</span></span>

## <span data-ttu-id="29e37-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29e37-132">RELATED LINKS</span></span>
