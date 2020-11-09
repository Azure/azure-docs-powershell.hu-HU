---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303872"
---
# <span data-ttu-id="2b133-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="2b133-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="2b133-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b133-102">SYNOPSIS</span></span>
<span data-ttu-id="2b133-103">Az API-kezelés nevű érték eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2b133-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="2b133-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b133-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b133-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b133-105">DESCRIPTION</span></span>
<span data-ttu-id="2b133-106">A **Remove-AzApiManagementNamedValue** parancsmag eltávolítja az Azure API-kezelés **nevű értéket**.</span><span class="sxs-lookup"><span data-stu-id="2b133-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="2b133-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b133-107">EXAMPLES</span></span>

### <span data-ttu-id="2b133-108">Példa 1: a névvel ellátott érték eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b133-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="2b133-109">Ez a parancs eltávolítja az azonosító Property11 tartalmazó névvel ellátott értéket.</span><span class="sxs-lookup"><span data-stu-id="2b133-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="2b133-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b133-110">PARAMETERS</span></span>

### <span data-ttu-id="2b133-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2b133-111">-Context</span></span>
<span data-ttu-id="2b133-112">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="2b133-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b133-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2b133-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2b133-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b133-114">-DefaultProfile</span></span>
<span data-ttu-id="2b133-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b133-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b133-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="2b133-116">-NamedValueId</span></span>
<span data-ttu-id="2b133-117">A meglévő névvel ellátott érték azonosítója</span><span class="sxs-lookup"><span data-stu-id="2b133-117">Identifier of existing named value.</span></span>
<span data-ttu-id="2b133-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2b133-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2b133-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b133-119">-PassThru</span></span>
<span data-ttu-id="2b133-120">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="2b133-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2b133-121">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2b133-121">This parameter is optional.</span></span>
<span data-ttu-id="2b133-122">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="2b133-122">Default value is false.</span></span>

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

### <span data-ttu-id="2b133-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b133-123">-Confirm</span></span>
<span data-ttu-id="2b133-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b133-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b133-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b133-125">-WhatIf</span></span>
<span data-ttu-id="2b133-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b133-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b133-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b133-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b133-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b133-128">CommonParameters</span></span>
<span data-ttu-id="2b133-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b133-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b133-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2b133-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b133-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b133-131">INPUTS</span></span>

### <span data-ttu-id="2b133-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b133-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b133-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2b133-133">System.String</span></span>

### <span data-ttu-id="2b133-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b133-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b133-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b133-135">OUTPUTS</span></span>

### <span data-ttu-id="2b133-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b133-136">System.Boolean</span></span>

## <span data-ttu-id="2b133-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b133-137">NOTES</span></span>

## <span data-ttu-id="2b133-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b133-138">RELATED LINKS</span></span>
