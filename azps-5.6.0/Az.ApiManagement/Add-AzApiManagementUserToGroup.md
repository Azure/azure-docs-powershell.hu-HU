---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: a56acc56bc100365f999ef1ca9a5f42f53b36096
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940665"
---
# <span data-ttu-id="5c682-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="5c682-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="5c682-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c682-102">SYNOPSIS</span></span>
<span data-ttu-id="5c682-103">Hozzáad egy felhasználót egy csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5c682-103">Adds a user to a group.</span></span>

## <span data-ttu-id="5c682-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c682-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c682-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c682-105">DESCRIPTION</span></span>
<span data-ttu-id="5c682-106">Az **Add-AzApiManagementUserToGroup** parancsmag hozzáad egy felhasználót egy csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5c682-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="5c682-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c682-107">EXAMPLES</span></span>

### <span data-ttu-id="5c682-108">1. példa: Felhasználó hozzáadása csoporthoz</span><span class="sxs-lookup"><span data-stu-id="5c682-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="5c682-109">Ez a parancs egy meglévő felhasználót ad hozzá egy meglévő csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="5c682-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="5c682-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c682-110">PARAMETERS</span></span>

### <span data-ttu-id="5c682-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5c682-111">-Context</span></span>
<span data-ttu-id="5c682-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="5c682-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5c682-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5c682-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5c682-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c682-114">-DefaultProfile</span></span>
<span data-ttu-id="5c682-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c682-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c682-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5c682-116">-GroupId</span></span>
<span data-ttu-id="5c682-117">A csoportazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c682-117">Specifies the group ID.</span></span>
<span data-ttu-id="5c682-118">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5c682-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5c682-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c682-119">-PassThru</span></span>
<span data-ttu-id="5c682-120">passthru</span><span class="sxs-lookup"><span data-stu-id="5c682-120">passthru</span></span>

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

### <span data-ttu-id="5c682-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="5c682-121">-UserId</span></span>
<span data-ttu-id="5c682-122">A felhasználóazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="5c682-122">Specifies the user ID.</span></span>
<span data-ttu-id="5c682-123">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="5c682-123">This parameter is required.</span></span>

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

### <span data-ttu-id="5c682-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c682-124">CommonParameters</span></span>
<span data-ttu-id="5c682-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c682-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c682-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c682-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c682-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c682-127">INPUTS</span></span>

### <span data-ttu-id="5c682-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5c682-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5c682-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5c682-129">System.String</span></span>

### <span data-ttu-id="5c682-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5c682-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5c682-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c682-131">OUTPUTS</span></span>

### <span data-ttu-id="5c682-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c682-132">System.Boolean</span></span>

## <span data-ttu-id="5c682-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c682-133">NOTES</span></span>

## <span data-ttu-id="5c682-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c682-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c682-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5c682-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="5c682-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="5c682-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


