---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 66d947cc9d5765fdbfeb815019bbd739f7c3d819
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504504"
---
# <span data-ttu-id="bf101-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="bf101-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="bf101-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf101-102">SYNOPSIS</span></span>
<span data-ttu-id="bf101-103">A NotificationHub tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="bf101-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf101-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf101-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf101-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf101-105">DESCRIPTION</span></span>
<span data-ttu-id="bf101-106">New-AzureRmNotificationHubKey parancsmag újragenerálja az NotificationHub-engedélyezési szabály elsődleges kulcsát/másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="bf101-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="bf101-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf101-107">EXAMPLES</span></span>

### <span data-ttu-id="bf101-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf101-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bf101-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="bf101-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bf101-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf101-110">PARAMETERS</span></span>

### <span data-ttu-id="bf101-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bf101-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf101-112">-DefaultProfile</span></span>
<span data-ttu-id="bf101-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bf101-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-114">-Force</span><span class="sxs-lookup"><span data-stu-id="bf101-114">-Force</span></span>
<span data-ttu-id="bf101-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf101-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf101-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bf101-117">-NotificationHub</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="bf101-118">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf101-119">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf101-120">-Confirm</span></span>
<span data-ttu-id="bf101-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf101-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf101-122">-WhatIf</span></span>
<span data-ttu-id="bf101-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf101-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf101-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf101-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf101-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf101-125">CommonParameters</span></span>
<span data-ttu-id="bf101-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf101-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf101-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf101-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf101-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf101-128">INPUTS</span></span>

### <span data-ttu-id="bf101-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="bf101-129">None</span></span>
<span data-ttu-id="bf101-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bf101-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf101-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf101-131">OUTPUTS</span></span>

### <span data-ttu-id="bf101-132">Microsoft. Azure. Management. NotificationHubs. models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="bf101-132">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="bf101-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf101-133">NOTES</span></span>

## <span data-ttu-id="bf101-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf101-134">RELATED LINKS</span></span>

