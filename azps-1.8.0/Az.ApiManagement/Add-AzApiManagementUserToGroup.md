---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 2d33ece97d2a0ef007b5970afef499fbb6f2117e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665709"
---
# <span data-ttu-id="db53c-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="db53c-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="db53c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db53c-102">SYNOPSIS</span></span>
<span data-ttu-id="db53c-103">Felhasználó felvétele egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="db53c-103">Adds a user to a group.</span></span>

## <span data-ttu-id="db53c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db53c-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db53c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db53c-105">DESCRIPTION</span></span>
<span data-ttu-id="db53c-106">Az **Add-AzApiManagementUserToGroup** parancsmag felvesz egy felhasználót egy csoportba.</span><span class="sxs-lookup"><span data-stu-id="db53c-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="db53c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db53c-107">EXAMPLES</span></span>

### <span data-ttu-id="db53c-108">1. példa: felhasználó felvétele egy csoportba</span><span class="sxs-lookup"><span data-stu-id="db53c-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="db53c-109">Ez a parancs egy meglévő felhasználót ad hozzá egy meglévő csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="db53c-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="db53c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db53c-110">PARAMETERS</span></span>

### <span data-ttu-id="db53c-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="db53c-111">-Context</span></span>
<span data-ttu-id="db53c-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="db53c-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="db53c-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="db53c-113">This parameter is required.</span></span>

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

### <span data-ttu-id="db53c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db53c-114">-DefaultProfile</span></span>
<span data-ttu-id="db53c-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db53c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db53c-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="db53c-116">-GroupId</span></span>
<span data-ttu-id="db53c-117">A csoport AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="db53c-117">Specifies the group ID.</span></span>
<span data-ttu-id="db53c-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="db53c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="db53c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db53c-119">-PassThru</span></span>
<span data-ttu-id="db53c-120">passthru</span><span class="sxs-lookup"><span data-stu-id="db53c-120">passthru</span></span>

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

### <span data-ttu-id="db53c-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="db53c-121">-UserId</span></span>
<span data-ttu-id="db53c-122">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="db53c-122">Specifies the user ID.</span></span>
<span data-ttu-id="db53c-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="db53c-123">This parameter is required.</span></span>

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

### <span data-ttu-id="db53c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db53c-124">CommonParameters</span></span>
<span data-ttu-id="db53c-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db53c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db53c-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db53c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db53c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db53c-127">INPUTS</span></span>

### <span data-ttu-id="db53c-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db53c-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db53c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db53c-129">System.String</span></span>

### <span data-ttu-id="db53c-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db53c-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db53c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db53c-131">OUTPUTS</span></span>

### <span data-ttu-id="db53c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db53c-132">System.Boolean</span></span>

## <span data-ttu-id="db53c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db53c-133">NOTES</span></span>

## <span data-ttu-id="db53c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db53c-134">RELATED LINKS</span></span>

[<span data-ttu-id="db53c-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="db53c-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="db53c-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="db53c-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


