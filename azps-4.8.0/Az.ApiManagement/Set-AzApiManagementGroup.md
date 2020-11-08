---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: f4e2bb2bce0dc01f99b55497ba671999c9c2ab01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025817"
---
# <span data-ttu-id="c3929-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c3929-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="c3929-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3929-102">SYNOPSIS</span></span>
<span data-ttu-id="c3929-103">API-kezelési csoport beállítása.</span><span class="sxs-lookup"><span data-stu-id="c3929-103">Configures an API management group.</span></span>

## <span data-ttu-id="c3929-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3929-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3929-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3929-105">DESCRIPTION</span></span>
<span data-ttu-id="c3929-106">A **set-AzApiManagementGroup** parancsmag API-kezelési csoportot állít be.</span><span class="sxs-lookup"><span data-stu-id="c3929-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="c3929-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c3929-107">EXAMPLES</span></span>

### <span data-ttu-id="c3929-108">Példa 1: felügyeleti csoport beállítása</span><span class="sxs-lookup"><span data-stu-id="c3929-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -GroupId "0001" -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="c3929-109">Ez a parancs a Group0001 nevű felügyeleti csoportot állítja be.</span><span class="sxs-lookup"><span data-stu-id="c3929-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="c3929-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3929-110">PARAMETERS</span></span>

### <span data-ttu-id="c3929-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c3929-111">-Context</span></span>
<span data-ttu-id="c3929-112">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3929-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c3929-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3929-113">-DefaultProfile</span></span>
<span data-ttu-id="c3929-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3929-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3929-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c3929-115">-Description</span></span>
<span data-ttu-id="c3929-116">A kezelési csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3929-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="c3929-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c3929-117">-GroupId</span></span>
<span data-ttu-id="c3929-118">A felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3929-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="c3929-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3929-119">-Name</span></span>
<span data-ttu-id="c3929-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3929-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="c3929-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3929-121">-PassThru</span></span>
<span data-ttu-id="c3929-122">passthru</span><span class="sxs-lookup"><span data-stu-id="c3929-122">passthru</span></span>

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

### <span data-ttu-id="c3929-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3929-123">-Confirm</span></span>
<span data-ttu-id="c3929-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3929-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3929-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3929-125">-WhatIf</span></span>
<span data-ttu-id="c3929-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3929-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3929-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3929-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3929-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3929-128">CommonParameters</span></span>
<span data-ttu-id="c3929-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3929-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3929-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3929-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3929-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3929-131">INPUTS</span></span>

### <span data-ttu-id="c3929-132">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c3929-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3929-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3929-133">System.String</span></span>

### <span data-ttu-id="c3929-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3929-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3929-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3929-135">OUTPUTS</span></span>

### <span data-ttu-id="c3929-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c3929-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="c3929-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3929-137">NOTES</span></span>

## <span data-ttu-id="c3929-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3929-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3929-139">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c3929-139">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="c3929-140">Új – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c3929-140">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="c3929-141">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c3929-141">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


