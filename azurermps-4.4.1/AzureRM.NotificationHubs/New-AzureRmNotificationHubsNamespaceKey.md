---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: ba33dd46a899f03539c39e61368570fb2bce0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494778"
---
# <span data-ttu-id="dcf12-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="dcf12-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="dcf12-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dcf12-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf12-103">Egy névtérhez tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="dcf12-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf12-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dcf12-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf12-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dcf12-105">DESCRIPTION</span></span>
<span data-ttu-id="dcf12-106">New-AzureRmNotificationHubNamespaceKey parancsmag újragenerálja a névtér-engedélyezési szabály elsődleges kulcsát/másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="dcf12-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="dcf12-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dcf12-107">EXAMPLES</span></span>

### <span data-ttu-id="dcf12-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dcf12-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="dcf12-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="dcf12-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="dcf12-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dcf12-110">PARAMETERS</span></span>

### <span data-ttu-id="dcf12-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dcf12-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="dcf12-112">-Force</span><span class="sxs-lookup"><span data-stu-id="dcf12-112">-Force</span></span>
<span data-ttu-id="dcf12-113">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dcf12-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dcf12-114">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dcf12-114">-Namespace</span></span>
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

### <span data-ttu-id="dcf12-115">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="dcf12-115">-PolicyKey</span></span>
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

### <span data-ttu-id="dcf12-116">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dcf12-116">-ResourceGroup</span></span>
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

### <span data-ttu-id="dcf12-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dcf12-117">-Confirm</span></span>
<span data-ttu-id="dcf12-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dcf12-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf12-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf12-119">-WhatIf</span></span>
<span data-ttu-id="dcf12-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dcf12-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf12-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcf12-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf12-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf12-122">-DefaultProfile</span></span>
<span data-ttu-id="dcf12-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcf12-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcf12-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf12-124">CommonParameters</span></span>
<span data-ttu-id="dcf12-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dcf12-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf12-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf12-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf12-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcf12-127">INPUTS</span></span>

## <span data-ttu-id="dcf12-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcf12-128">OUTPUTS</span></span>

### <span data-ttu-id="dcf12-129">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="dcf12-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="dcf12-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dcf12-130">NOTES</span></span>

## <span data-ttu-id="dcf12-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcf12-131">RELATED LINKS</span></span>

