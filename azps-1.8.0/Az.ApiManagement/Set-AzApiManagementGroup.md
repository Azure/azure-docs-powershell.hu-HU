---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementGroup.md
ms.openlocfilehash: 027e07ed495cb5b80fbd05852b640526c87bf16e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836913"
---
# <span data-ttu-id="b476e-101">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b476e-101">Set-AzApiManagementGroup</span></span>

## <span data-ttu-id="b476e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b476e-102">SYNOPSIS</span></span>
<span data-ttu-id="b476e-103">API-kezelési csoport beállítása.</span><span class="sxs-lookup"><span data-stu-id="b476e-103">Configures an API management group.</span></span>

## <span data-ttu-id="b476e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b476e-104">SYNTAX</span></span>

```
Set-AzApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b476e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b476e-105">DESCRIPTION</span></span>
<span data-ttu-id="b476e-106">A **set-AzApiManagementGroup** parancsmag API-kezelési csoportot állít be.</span><span class="sxs-lookup"><span data-stu-id="b476e-106">The **Set-AzApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="b476e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b476e-107">EXAMPLES</span></span>

### <span data-ttu-id="b476e-108">Példa 1: felügyeleti csoport beállítása</span><span class="sxs-lookup"><span data-stu-id="b476e-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="b476e-109">Ez a parancs a Group0001 nevű felügyeleti csoportot állítja be.</span><span class="sxs-lookup"><span data-stu-id="b476e-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="b476e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b476e-110">PARAMETERS</span></span>

### <span data-ttu-id="b476e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b476e-111">-Context</span></span>
<span data-ttu-id="b476e-112">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b476e-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b476e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b476e-113">-DefaultProfile</span></span>
<span data-ttu-id="b476e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b476e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b476e-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b476e-115">-Description</span></span>
<span data-ttu-id="b476e-116">A kezelési csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b476e-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="b476e-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b476e-117">-GroupId</span></span>
<span data-ttu-id="b476e-118">A felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b476e-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="b476e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b476e-119">-Name</span></span>
<span data-ttu-id="b476e-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b476e-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="b476e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b476e-121">-PassThru</span></span>
<span data-ttu-id="b476e-122">passthru</span><span class="sxs-lookup"><span data-stu-id="b476e-122">passthru</span></span>

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

### <span data-ttu-id="b476e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b476e-123">CommonParameters</span></span>
<span data-ttu-id="b476e-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b476e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b476e-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b476e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b476e-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b476e-126">INPUTS</span></span>

### <span data-ttu-id="b476e-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b476e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b476e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b476e-128">System.String</span></span>

### <span data-ttu-id="b476e-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b476e-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b476e-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b476e-130">OUTPUTS</span></span>

### <span data-ttu-id="b476e-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b476e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="b476e-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b476e-132">NOTES</span></span>

## <span data-ttu-id="b476e-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b476e-133">RELATED LINKS</span></span>

[<span data-ttu-id="b476e-134">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b476e-134">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="b476e-135">Új – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b476e-135">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="b476e-136">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b476e-136">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)


