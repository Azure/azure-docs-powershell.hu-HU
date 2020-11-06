---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1a3fd2ca25099be029616e048c5ebfa0e398229e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492064"
---
# <span data-ttu-id="42604-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42604-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="42604-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42604-102">SYNOPSIS</span></span>
<span data-ttu-id="42604-103">Eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="42604-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42604-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42604-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42604-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42604-105">DESCRIPTION</span></span>
<span data-ttu-id="42604-106">A **Remove-AzureRmApiManagementOperation** parancsmag eltávolítja a meglévő műveletet.</span><span class="sxs-lookup"><span data-stu-id="42604-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="42604-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42604-107">EXAMPLES</span></span>

### <span data-ttu-id="42604-108">1. példa: meglévő API-művelet eltávolítása</span><span class="sxs-lookup"><span data-stu-id="42604-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="42604-109">Ez a parancs eltávolítja a meglévő API-műveletet.</span><span class="sxs-lookup"><span data-stu-id="42604-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="42604-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42604-110">PARAMETERS</span></span>

### <span data-ttu-id="42604-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="42604-111">-ApiId</span></span>
<span data-ttu-id="42604-112">Az API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42604-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="42604-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="42604-113">-ApiRevision</span></span>
<span data-ttu-id="42604-114">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="42604-114">Identifier of API Revision.</span></span> <span data-ttu-id="42604-115">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="42604-115">This parameter is optional.</span></span> <span data-ttu-id="42604-116">Ha nem adja meg, akkor a művelet törlődik a jelenleg aktív API-verzióból.</span><span class="sxs-lookup"><span data-stu-id="42604-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="42604-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="42604-117">-Context</span></span>
<span data-ttu-id="42604-118">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="42604-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="42604-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42604-119">-DefaultProfile</span></span>
<span data-ttu-id="42604-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42604-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42604-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="42604-121">-OperationId</span></span>
<span data-ttu-id="42604-122">Az API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="42604-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="42604-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42604-123">-PassThru</span></span>
<span data-ttu-id="42604-124">Azt jelzi, hogy ez a parancsmag az $True értékét adja eredményül, ha a művelet sikeres, vagy ha a $False értéke egyébként nem.</span><span class="sxs-lookup"><span data-stu-id="42604-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="42604-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42604-125">-Confirm</span></span>
<span data-ttu-id="42604-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42604-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42604-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42604-127">-WhatIf</span></span>
<span data-ttu-id="42604-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42604-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42604-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42604-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42604-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42604-130">CommonParameters</span></span>
<span data-ttu-id="42604-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42604-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42604-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42604-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42604-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42604-133">INPUTS</span></span>

### <span data-ttu-id="42604-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42604-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42604-135">System. String</span><span class="sxs-lookup"><span data-stu-id="42604-135">System.String</span></span>

### <span data-ttu-id="42604-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42604-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42604-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42604-137">OUTPUTS</span></span>

### <span data-ttu-id="42604-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42604-138">System.Boolean</span></span>

## <span data-ttu-id="42604-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42604-139">NOTES</span></span>

## <span data-ttu-id="42604-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42604-140">RELATED LINKS</span></span>

[<span data-ttu-id="42604-141">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42604-141">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="42604-142">Új – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42604-142">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="42604-143">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="42604-143">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


