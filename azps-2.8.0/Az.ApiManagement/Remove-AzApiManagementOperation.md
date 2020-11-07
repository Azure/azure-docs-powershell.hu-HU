---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: b5d52c4fa70312e276851cb3043c7dbd7babdc1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667980"
---
# <span data-ttu-id="7aac0-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7aac0-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="7aac0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7aac0-102">SYNOPSIS</span></span>
<span data-ttu-id="7aac0-103">Eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="7aac0-103">Removes an existing operation.</span></span>

## <span data-ttu-id="7aac0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7aac0-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7aac0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7aac0-105">DESCRIPTION</span></span>
<span data-ttu-id="7aac0-106">A **Remove-AzApiManagementOperation** parancsmag eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="7aac0-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="7aac0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7aac0-107">EXAMPLES</span></span>

### <span data-ttu-id="7aac0-108">1. példa: meglévő API-művelet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7aac0-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="7aac0-109">Ez a parancs eltávolítja a meglévő API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="7aac0-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="7aac0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7aac0-110">PARAMETERS</span></span>

### <span data-ttu-id="7aac0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7aac0-111">-ApiId</span></span>
<span data-ttu-id="7aac0-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aac0-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="7aac0-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="7aac0-113">-ApiRevision</span></span>
<span data-ttu-id="7aac0-114">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="7aac0-114">Identifier of API Revision.</span></span> <span data-ttu-id="7aac0-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="7aac0-115">This parameter is optional.</span></span> <span data-ttu-id="7aac0-116">Ha nem adja meg, akkor a művelet törlődik a jelenleg aktív API-verzióból.</span><span class="sxs-lookup"><span data-stu-id="7aac0-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="7aac0-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7aac0-117">-Context</span></span>
<span data-ttu-id="7aac0-118">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aac0-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="7aac0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aac0-119">-DefaultProfile</span></span>
<span data-ttu-id="7aac0-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7aac0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aac0-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="7aac0-121">-OperationId</span></span>
<span data-ttu-id="7aac0-122">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7aac0-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="7aac0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7aac0-123">-PassThru</span></span>
<span data-ttu-id="7aac0-124">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha a $False értéke egyébként nem.</span><span class="sxs-lookup"><span data-stu-id="7aac0-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="7aac0-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7aac0-125">-Confirm</span></span>
<span data-ttu-id="7aac0-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7aac0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aac0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aac0-127">-WhatIf</span></span>
<span data-ttu-id="7aac0-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7aac0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aac0-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aac0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aac0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aac0-130">CommonParameters</span></span>
<span data-ttu-id="7aac0-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7aac0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aac0-132">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7aac0-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aac0-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aac0-133">INPUTS</span></span>

### <span data-ttu-id="7aac0-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7aac0-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7aac0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7aac0-135">System.String</span></span>

### <span data-ttu-id="7aac0-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7aac0-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7aac0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aac0-137">OUTPUTS</span></span>

### <span data-ttu-id="7aac0-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7aac0-138">System.Boolean</span></span>

## <span data-ttu-id="7aac0-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7aac0-139">NOTES</span></span>

## <span data-ttu-id="7aac0-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aac0-140">RELATED LINKS</span></span>

[<span data-ttu-id="7aac0-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7aac0-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="7aac0-142">Új – AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7aac0-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="7aac0-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7aac0-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


