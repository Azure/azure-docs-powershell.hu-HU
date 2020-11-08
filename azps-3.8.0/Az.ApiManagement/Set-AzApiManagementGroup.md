---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013856"
---
# <span data-ttu-id="f1632-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1632-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="f1632-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1632-102">SYNOPSIS</span></span>
<span data-ttu-id="f1632-103">API-kezelési csoport beállítása.</span><span class="sxs-lookup"><span data-stu-id="f1632-103">Configures an API management group.</span></span>

## <span data-ttu-id="f1632-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1632-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1632-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1632-105">DESCRIPTION</span></span>
<span data-ttu-id="f1632-106">A **set-AzApiManagementGroup** parancsmag API-kezelési csoportot állít be.</span><span class="sxs-lookup"><span data-stu-id="f1632-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="f1632-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1632-107">EXAMPLES</span></span>

### <span data-ttu-id="f1632-108">Példa 1: felügyeleti csoport beállítása</span><span class="sxs-lookup"><span data-stu-id="f1632-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="f1632-109">Ez a parancs a Group0001 nevű felügyeleti csoportot állítja be.</span><span class="sxs-lookup"><span data-stu-id="f1632-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="f1632-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1632-110">PARAMETERS</span></span>

### <span data-ttu-id="f1632-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f1632-111">-Context</span></span>
<span data-ttu-id="f1632-112">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1632-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1632-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1632-113">-DefaultProfile</span></span>
<span data-ttu-id="f1632-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1632-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1632-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f1632-115">-Description</span></span>
<span data-ttu-id="f1632-116">A kezelési csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1632-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="f1632-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f1632-117">-GroupId</span></span>
<span data-ttu-id="f1632-118">A felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1632-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="f1632-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1632-119">-Name</span></span>
<span data-ttu-id="f1632-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f1632-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="f1632-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1632-121">-PassThru</span></span>
<span data-ttu-id="f1632-122">passthru</span><span class="sxs-lookup"><span data-stu-id="f1632-122">passthru</span></span>

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

### <span data-ttu-id="f1632-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1632-123">-Confirm</span></span>
<span data-ttu-id="f1632-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1632-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1632-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1632-125">-WhatIf</span></span>
<span data-ttu-id="f1632-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1632-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1632-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1632-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1632-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1632-128">CommonParameters</span></span>
<span data-ttu-id="f1632-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1632-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1632-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f1632-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1632-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1632-131">INPUTS</span></span>

### <span data-ttu-id="f1632-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1632-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1632-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f1632-133">System.String</span></span>

### <span data-ttu-id="f1632-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1632-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1632-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1632-135">OUTPUTS</span></span>

### <span data-ttu-id="f1632-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1632-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="f1632-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1632-137">NOTES</span></span>

## <span data-ttu-id="f1632-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1632-138">RELATED LINKS</span></span>

[<span data-ttu-id="f1632-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1632-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="f1632-140">Új – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1632-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="f1632-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1632-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


