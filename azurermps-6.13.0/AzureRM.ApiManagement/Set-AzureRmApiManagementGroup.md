---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492919"
---
# <span data-ttu-id="09911-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09911-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="09911-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09911-102">SYNOPSIS</span></span>
<span data-ttu-id="09911-103">API-kezelési csoport beállítása.</span><span class="sxs-lookup"><span data-stu-id="09911-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09911-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09911-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09911-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09911-105">DESCRIPTION</span></span>
<span data-ttu-id="09911-106">A **set-AzureRmApiManagementGroup** parancsmag API-kezelési csoportot állít be.</span><span class="sxs-lookup"><span data-stu-id="09911-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="09911-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09911-107">EXAMPLES</span></span>

### <span data-ttu-id="09911-108">Példa 1: felügyeleti csoport beállítása</span><span class="sxs-lookup"><span data-stu-id="09911-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="09911-109">Ez a parancs a Group0001 nevű felügyeleti csoportot állítja be.</span><span class="sxs-lookup"><span data-stu-id="09911-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="09911-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09911-110">PARAMETERS</span></span>

### <span data-ttu-id="09911-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="09911-111">-Context</span></span>
<span data-ttu-id="09911-112">Egy **PsApiManagementContext** -objektum példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09911-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="09911-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09911-113">-DefaultProfile</span></span>
<span data-ttu-id="09911-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09911-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09911-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="09911-115">-Description</span></span>
<span data-ttu-id="09911-116">A kezelési csoport leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="09911-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="09911-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="09911-117">-GroupId</span></span>
<span data-ttu-id="09911-118">A felügyeleti csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09911-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="09911-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="09911-119">-Name</span></span>
<span data-ttu-id="09911-120">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09911-120">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="09911-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09911-121">-PassThru</span></span>
<span data-ttu-id="09911-122">passthru</span><span class="sxs-lookup"><span data-stu-id="09911-122">passthru</span></span>

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

### <span data-ttu-id="09911-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09911-123">CommonParameters</span></span>
<span data-ttu-id="09911-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09911-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09911-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09911-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09911-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09911-126">INPUTS</span></span>

### <span data-ttu-id="09911-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09911-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09911-128">System. String</span><span class="sxs-lookup"><span data-stu-id="09911-128">System.String</span></span>

### <span data-ttu-id="09911-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="09911-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="09911-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09911-130">OUTPUTS</span></span>

### <span data-ttu-id="09911-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09911-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="09911-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09911-132">NOTES</span></span>

## <span data-ttu-id="09911-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09911-133">RELATED LINKS</span></span>

[<span data-ttu-id="09911-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09911-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="09911-135">Új – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09911-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="09911-136">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="09911-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


