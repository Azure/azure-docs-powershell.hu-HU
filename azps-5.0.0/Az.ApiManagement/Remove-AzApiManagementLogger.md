---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 98AD1C84-B147-48EB-94B5-8D77B531F6F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementLogger.md
ms.openlocfilehash: e68fec8bf38dc990737f11d5dc3ed079d71fd6ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188147"
---
# <span data-ttu-id="66487-101">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66487-101">Remove-AzApiManagementLogger</span></span>

## <span data-ttu-id="66487-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66487-102">SYNOPSIS</span></span>
<span data-ttu-id="66487-103">API-kezelési naplózó eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="66487-103">Removes an API Management Logger.</span></span>

## <span data-ttu-id="66487-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66487-104">SYNTAX</span></span>

```
Remove-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66487-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66487-105">DESCRIPTION</span></span>
<span data-ttu-id="66487-106">A **Remove-AzApiManagementLogger** parancsmag egy Azure API-kezelési **naplózó** eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="66487-106">The **Remove-AzApiManagementLogger** cmdlet removes an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="66487-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66487-107">EXAMPLES</span></span>

### <span data-ttu-id="66487-108">1. példa: naplózó eltávolítása</span><span class="sxs-lookup"><span data-stu-id="66487-108">Example 1: Remove a logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Force
```

<span data-ttu-id="66487-109">Ez a parancs eltávolítja az azonosító Logger123 tartalmazó naplózó.</span><span class="sxs-lookup"><span data-stu-id="66487-109">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="66487-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66487-110">PARAMETERS</span></span>

### <span data-ttu-id="66487-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="66487-111">-Context</span></span>
<span data-ttu-id="66487-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="66487-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="66487-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66487-113">-DefaultProfile</span></span>
<span data-ttu-id="66487-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66487-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66487-115">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="66487-115">-LoggerId</span></span>
<span data-ttu-id="66487-116">Az eltávolítandó naplózó AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="66487-116">Specifies the ID of the logger to remove.</span></span>

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

### <span data-ttu-id="66487-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66487-117">-PassThru</span></span>
<span data-ttu-id="66487-118">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="66487-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="66487-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66487-119">-Confirm</span></span>
<span data-ttu-id="66487-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66487-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66487-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66487-121">-WhatIf</span></span>
<span data-ttu-id="66487-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66487-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66487-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66487-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66487-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66487-124">CommonParameters</span></span>
<span data-ttu-id="66487-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66487-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66487-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66487-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66487-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66487-127">INPUTS</span></span>

### <span data-ttu-id="66487-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66487-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66487-129">System. String</span><span class="sxs-lookup"><span data-stu-id="66487-129">System.String</span></span>

### <span data-ttu-id="66487-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66487-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66487-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66487-131">OUTPUTS</span></span>

### <span data-ttu-id="66487-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66487-132">System.Boolean</span></span>

## <span data-ttu-id="66487-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66487-133">NOTES</span></span>

## <span data-ttu-id="66487-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66487-134">RELATED LINKS</span></span>

[<span data-ttu-id="66487-135">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66487-135">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="66487-136">Új – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66487-136">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="66487-137">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="66487-137">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)

