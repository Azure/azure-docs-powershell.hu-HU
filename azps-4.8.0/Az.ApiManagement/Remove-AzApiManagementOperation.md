---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024247"
---
# <span data-ttu-id="37c53-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="37c53-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="37c53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="37c53-102">SYNOPSIS</span></span>
<span data-ttu-id="37c53-103">Eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="37c53-103">Removes an existing operation.</span></span>

## <span data-ttu-id="37c53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="37c53-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37c53-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="37c53-105">DESCRIPTION</span></span>
<span data-ttu-id="37c53-106">A **Remove-AzApiManagementOperation** parancsmag eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="37c53-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="37c53-107">Példák</span><span class="sxs-lookup"><span data-stu-id="37c53-107">EXAMPLES</span></span>

### <span data-ttu-id="37c53-108">1. példa: meglévő API-művelet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="37c53-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="37c53-109">Ez a parancs eltávolítja a meglévő API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="37c53-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="37c53-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="37c53-110">PARAMETERS</span></span>

### <span data-ttu-id="37c53-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="37c53-111">-ApiId</span></span>
<span data-ttu-id="37c53-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="37c53-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="37c53-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="37c53-113">-ApiRevision</span></span>
<span data-ttu-id="37c53-114">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="37c53-114">Identifier of API Revision.</span></span> <span data-ttu-id="37c53-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="37c53-115">This parameter is optional.</span></span> <span data-ttu-id="37c53-116">Ha nem adja meg, akkor a művelet törlődik a jelenleg aktív API-verzióból.</span><span class="sxs-lookup"><span data-stu-id="37c53-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37c53-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="37c53-117">-Context</span></span>
<span data-ttu-id="37c53-118">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="37c53-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="37c53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c53-119">-DefaultProfile</span></span>
<span data-ttu-id="37c53-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="37c53-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37c53-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="37c53-121">-OperationId</span></span>
<span data-ttu-id="37c53-122">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="37c53-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="37c53-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37c53-123">-PassThru</span></span>
<span data-ttu-id="37c53-124">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha a $False értéke egyébként nem.</span><span class="sxs-lookup"><span data-stu-id="37c53-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="37c53-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="37c53-125">-Confirm</span></span>
<span data-ttu-id="37c53-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="37c53-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c53-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c53-127">-WhatIf</span></span>
<span data-ttu-id="37c53-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="37c53-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c53-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="37c53-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c53-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c53-130">CommonParameters</span></span>
<span data-ttu-id="37c53-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="37c53-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c53-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="37c53-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c53-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c53-133">INPUTS</span></span>

### <span data-ttu-id="37c53-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="37c53-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37c53-135">System. String</span><span class="sxs-lookup"><span data-stu-id="37c53-135">System.String</span></span>

### <span data-ttu-id="37c53-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37c53-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37c53-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="37c53-137">OUTPUTS</span></span>

### <span data-ttu-id="37c53-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37c53-138">System.Boolean</span></span>

## <span data-ttu-id="37c53-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="37c53-139">NOTES</span></span>

## <span data-ttu-id="37c53-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="37c53-140">RELATED LINKS</span></span>

[<span data-ttu-id="37c53-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="37c53-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="37c53-142">Új – AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="37c53-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="37c53-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="37c53-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


