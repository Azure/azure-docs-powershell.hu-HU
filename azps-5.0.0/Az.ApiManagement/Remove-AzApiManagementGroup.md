---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B88EC6DB-84AC-4F1D-AD79-0D243E0DC88A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGroup.md
ms.openlocfilehash: 73e1fbee1dd20a9a30260727f693376346c87f0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188151"
---
# <span data-ttu-id="b9ed6-101">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b9ed6-101">Remove-AzApiManagementGroup</span></span>

## <span data-ttu-id="b9ed6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ed6-103">Egy meglévő API-kezelési csoport eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-103">Removes an existing API management group.</span></span>

## <span data-ttu-id="b9ed6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9ed6-104">SYNTAX</span></span>

```
Remove-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ed6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="b9ed6-106">A **Remove-AzApiManagementGroup** parancsmag egy meglévő API-kezelési csoport eltávolítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-106">The **Remove-AzApiManagementGroup** cmdlet removes an existing API management group.</span></span>

## <span data-ttu-id="b9ed6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="b9ed6-108">1. példa: meglévő felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b9ed6-108">Example 1: Remove an existing management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGroup -Context $apimContext -GroupId "Group0001" -Force
```

<span data-ttu-id="b9ed6-109">Ez a parancs eltávolítja a Group0001 nevű meglévő felügyeleti csoportot, és nem kéri a felhasználótól a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-109">This command removes an existing management group named Group0001 and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="b9ed6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9ed6-110">PARAMETERS</span></span>

### <span data-ttu-id="b9ed6-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b9ed6-111">-Context</span></span>
<span data-ttu-id="b9ed6-112">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-112">Specifies the instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ed6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ed6-113">-DefaultProfile</span></span>
<span data-ttu-id="b9ed6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9ed6-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b9ed6-115">-GroupId</span></span>
<span data-ttu-id="b9ed6-116">A felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-116">Specifies the identifier of a management group.</span></span>

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

### <span data-ttu-id="b9ed6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9ed6-117">-PassThru</span></span>
<span data-ttu-id="b9ed6-118">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha a $False értéke egyébként nem.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b9ed6-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9ed6-119">-Confirm</span></span>
<span data-ttu-id="b9ed6-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ed6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ed6-121">-WhatIf</span></span>
<span data-ttu-id="b9ed6-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ed6-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ed6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ed6-124">CommonParameters</span></span>
<span data-ttu-id="b9ed6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9ed6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ed6-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b9ed6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ed6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9ed6-127">INPUTS</span></span>

### <span data-ttu-id="b9ed6-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9ed6-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b9ed6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b9ed6-129">System.String</span></span>

### <span data-ttu-id="b9ed6-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b9ed6-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b9ed6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9ed6-131">OUTPUTS</span></span>

### <span data-ttu-id="b9ed6-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9ed6-132">System.Boolean</span></span>

## <span data-ttu-id="b9ed6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9ed6-133">NOTES</span></span>

## <span data-ttu-id="b9ed6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9ed6-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9ed6-135">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b9ed6-135">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="b9ed6-136">Új – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b9ed6-136">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="b9ed6-137">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b9ed6-137">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


