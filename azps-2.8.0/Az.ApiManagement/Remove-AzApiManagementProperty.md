---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D3C60123-CE1F-45F1-8C8F-25CDC302490C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProperty.md
ms.openlocfilehash: 323cbbdc38281c9b90ab3728eb2879bf1b7bfe89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667969"
---
# <span data-ttu-id="d6e5a-101">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d6e5a-101">Remove-AzApiManagementProperty</span></span>

## <span data-ttu-id="d6e5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6e5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e5a-103">Egy API-kezelési tulajdonság eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-103">Removes an API Management Property.</span></span>

## <span data-ttu-id="d6e5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6e5a-104">SYNTAX</span></span>

```
Remove-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6e5a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6e5a-105">DESCRIPTION</span></span>
<span data-ttu-id="d6e5a-106">A **Remove-AzApiManagementProperty** parancsmag eltávolítja az Azure API Management **tulajdonságot**.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-106">The **Remove-AzApiManagementProperty** cmdlet removes an Azure API Management **Property**.</span></span>

## <span data-ttu-id="d6e5a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6e5a-107">EXAMPLES</span></span>

### <span data-ttu-id="d6e5a-108">1. példa: tulajdonság eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d6e5a-108">Example 1: Remove a property</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -PassThru
```

<span data-ttu-id="d6e5a-109">Ez a parancs eltávolítja az ID Property11 tartalmazó tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-109">This command removes the property that has the ID Property11.</span></span>

## <span data-ttu-id="d6e5a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6e5a-110">PARAMETERS</span></span>

### <span data-ttu-id="d6e5a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d6e5a-111">-Context</span></span>
<span data-ttu-id="d6e5a-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d6e5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6e5a-113">-DefaultProfile</span></span>
<span data-ttu-id="d6e5a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6e5a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6e5a-115">-PassThru</span></span>
<span data-ttu-id="d6e5a-116">Azt jelzi, hogy ez a parancsmag $True értéket ad eredményül, ha a művelet sikerül vagy $False más módon.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="d6e5a-117">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="d6e5a-117">-PropertyId</span></span>
<span data-ttu-id="d6e5a-118">A parancsmag által eltávolított tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-118">Specifies an ID of the property that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d6e5a-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6e5a-119">-Confirm</span></span>
<span data-ttu-id="d6e5a-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6e5a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6e5a-121">-WhatIf</span></span>
<span data-ttu-id="d6e5a-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6e5a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6e5a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e5a-124">CommonParameters</span></span>
<span data-ttu-id="d6e5a-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6e5a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e5a-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6e5a-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e5a-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e5a-127">INPUTS</span></span>

### <span data-ttu-id="d6e5a-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6e5a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6e5a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d6e5a-129">System.String</span></span>

### <span data-ttu-id="d6e5a-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d6e5a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6e5a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6e5a-131">OUTPUTS</span></span>

### <span data-ttu-id="d6e5a-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6e5a-132">System.Boolean</span></span>

## <span data-ttu-id="d6e5a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6e5a-133">NOTES</span></span>

## <span data-ttu-id="d6e5a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6e5a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d6e5a-135">Új – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d6e5a-135">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="d6e5a-136">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="d6e5a-136">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


