---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementGroup.md
ms.openlocfilehash: 6a866932d5fa46c621e4ac67e5147650dc1dbc28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493895"
---
# <span data-ttu-id="ce6ec-101">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ce6ec-101">Remove-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="ce6ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6ec-103">Egy meglévő API-kezelési csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-103">Removes an existing API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce6ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce6ec-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce6ec-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce6ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6ec-106">A **Remove-AzureRmApiManagementGroup** parancsmag egy meglévő API-kezelési csoport eltávolítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-106">The **Remove-AzureRmApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="ce6ec-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ce6ec-107">EXAMPLES</span></span>

### <span data-ttu-id="ce6ec-108">1. példa: meglévő felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ce6ec-108">Example 1: Remove an existing management group</span></span>
```
PS C:\>Remove-AzureRmApiManagementGroup -Context $APImContext -GroupId "Group0001" -Force
```

<span data-ttu-id="ce6ec-109">Ez a parancs eltávolítja a Group0001 nevű meglévő felügyeleti csoportot, és nem kéri a felhasználótól a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="ce6ec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce6ec-110">PARAMETERS</span></span>

### <span data-ttu-id="ce6ec-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ce6ec-111">-Context</span></span>
<span data-ttu-id="ce6ec-112">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6ec-113">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ce6ec-113">-GroupId</span></span>
<span data-ttu-id="ce6ec-114">A felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-114">Specifies the identifier of a management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6ec-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce6ec-115">-PassThru</span></span>
<span data-ttu-id="ce6ec-116">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha a $False értéke egyébként nem.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-116">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6ec-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce6ec-117">-Confirm</span></span>
<span data-ttu-id="ce6ec-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6ec-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce6ec-119">-WhatIf</span></span>
<span data-ttu-id="ce6ec-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce6ec-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6ec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6ec-122">-DefaultProfile</span></span>
<span data-ttu-id="ce6ec-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce6ec-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce6ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6ec-124">CommonParameters</span></span>
<span data-ttu-id="ce6ec-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce6ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6ec-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6ec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6ec-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce6ec-127">INPUTS</span></span>

## <span data-ttu-id="ce6ec-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce6ec-128">OUTPUTS</span></span>

### <span data-ttu-id="ce6ec-129">Logikai</span><span class="sxs-lookup"><span data-stu-id="ce6ec-129">Boolean</span></span>

## <span data-ttu-id="ce6ec-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce6ec-130">NOTES</span></span>

## <span data-ttu-id="ce6ec-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce6ec-131">RELATED LINKS</span></span>

[<span data-ttu-id="ce6ec-132">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ce6ec-132">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="ce6ec-133">Új – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ce6ec-133">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="ce6ec-134">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ce6ec-134">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


