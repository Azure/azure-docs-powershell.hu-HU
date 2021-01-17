---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350670"
---
# <span data-ttu-id="0dd36-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="0dd36-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="0dd36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dd36-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd36-103">A NotificationHub engedélyezési szabálykulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="0dd36-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="0dd36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0dd36-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd36-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0dd36-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd36-106">New-AzNotificationHubKey parancsmag újragenerálja az NotificationHub engedélyezési szabály elsődleges kulcsát/másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="0dd36-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="0dd36-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0dd36-107">EXAMPLES</span></span>

### <span data-ttu-id="0dd36-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0dd36-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0dd36-109">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="0dd36-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0dd36-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0dd36-110">PARAMETERS</span></span>

### <span data-ttu-id="0dd36-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0dd36-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="0dd36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd36-112">-DefaultProfile</span></span>
<span data-ttu-id="0dd36-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0dd36-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dd36-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd36-114">-Force</span></span>
<span data-ttu-id="0dd36-115">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0dd36-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0dd36-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0dd36-116">-Namespace</span></span>
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

### <span data-ttu-id="0dd36-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0dd36-117">-NotificationHub</span></span>
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

### <span data-ttu-id="0dd36-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="0dd36-118">-PolicyKey</span></span>
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

### <span data-ttu-id="0dd36-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0dd36-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="0dd36-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dd36-120">-Confirm</span></span>
<span data-ttu-id="0dd36-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0dd36-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dd36-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd36-122">-WhatIf</span></span>
<span data-ttu-id="0dd36-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0dd36-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dd36-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0dd36-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dd36-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd36-125">CommonParameters</span></span>
<span data-ttu-id="0dd36-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd36-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd36-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd36-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd36-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0dd36-128">INPUTS</span></span>

### <span data-ttu-id="0dd36-129">System.String</span><span class="sxs-lookup"><span data-stu-id="0dd36-129">System.String</span></span>

## <span data-ttu-id="0dd36-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0dd36-130">OUTPUTS</span></span>

### <span data-ttu-id="0dd36-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="0dd36-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="0dd36-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0dd36-132">NOTES</span></span>

## <span data-ttu-id="0dd36-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0dd36-133">RELATED LINKS</span></span>
