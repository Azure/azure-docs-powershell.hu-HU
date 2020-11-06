---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 419dd6efcf9152c03d3f94f5ab9ead06c3c234ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497019"
---
# <span data-ttu-id="b21a3-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="b21a3-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="b21a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b21a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b21a3-103">A NotificationHub tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="b21a3-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b21a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b21a3-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b21a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b21a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b21a3-106">New-AzureRmNotificationHubKey parancsmag újragenerálja az NotificationHub-engedélyezési szabály elsődleges kulcsát/másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="b21a3-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="b21a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b21a3-107">EXAMPLES</span></span>

### <span data-ttu-id="b21a3-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b21a3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b21a3-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="b21a3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b21a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b21a3-110">PARAMETERS</span></span>

### <span data-ttu-id="b21a3-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b21a3-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b21a3-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b21a3-112">-Force</span></span>
<span data-ttu-id="b21a3-113">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b21a3-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b21a3-114">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b21a3-114">-Namespace</span></span>
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

### <span data-ttu-id="b21a3-115">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b21a3-115">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b21a3-116">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="b21a3-116">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21a3-117">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b21a3-117">-ResourceGroup</span></span>
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

### <span data-ttu-id="b21a3-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b21a3-118">-Confirm</span></span>
<span data-ttu-id="b21a3-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b21a3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b21a3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21a3-120">-WhatIf</span></span>
<span data-ttu-id="b21a3-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b21a3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21a3-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b21a3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b21a3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b21a3-123">-DefaultProfile</span></span>
<span data-ttu-id="b21a3-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b21a3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b21a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21a3-125">CommonParameters</span></span>
<span data-ttu-id="b21a3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b21a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21a3-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b21a3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21a3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b21a3-128">INPUTS</span></span>

## <span data-ttu-id="b21a3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b21a3-129">OUTPUTS</span></span>

### <span data-ttu-id="b21a3-130">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="b21a3-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="b21a3-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b21a3-131">NOTES</span></span>

## <span data-ttu-id="b21a3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b21a3-132">RELATED LINKS</span></span>

