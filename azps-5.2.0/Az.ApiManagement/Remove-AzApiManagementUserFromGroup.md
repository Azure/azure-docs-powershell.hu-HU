---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339786"
---
# <span data-ttu-id="ecbd8-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="ecbd8-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="ecbd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="ecbd8-103">Eltávolít egy felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-103">Removes a user from a group.</span></span>

## <span data-ttu-id="ecbd8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecbd8-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecbd8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecbd8-105">DESCRIPTION</span></span>
<span data-ttu-id="ecbd8-106">A **Remove-AzApiManagementUserFromGroup** parancsmag eltávolít egy felhasználót egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="ecbd8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecbd8-107">EXAMPLES</span></span>

### <span data-ttu-id="ecbd8-108">1. példa: Felhasználó eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="ecbd8-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="ecbd8-109">Ez a parancs eltávolítja a felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="ecbd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecbd8-110">PARAMETERS</span></span>

### <span data-ttu-id="ecbd8-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ecbd8-111">-Context</span></span>
<span data-ttu-id="ecbd8-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ecbd8-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ecbd8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecbd8-114">-DefaultProfile</span></span>
<span data-ttu-id="ecbd8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecbd8-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ecbd8-116">-GroupId</span></span>
<span data-ttu-id="ecbd8-117">Annak a csoportnak az azonosítója, amelyből a felhasználót el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="ecbd8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecbd8-118">-PassThru</span></span>
<span data-ttu-id="ecbd8-119">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy egy $False értéket.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ecbd8-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="ecbd8-120">-UserId</span></span>
<span data-ttu-id="ecbd8-121">A csoportból eltávolítható felhasználó azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="ecbd8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecbd8-122">CommonParameters</span></span>
<span data-ttu-id="ecbd8-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecbd8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecbd8-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecbd8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecbd8-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecbd8-125">INPUTS</span></span>

### <span data-ttu-id="ecbd8-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ecbd8-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ecbd8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ecbd8-127">System.String</span></span>

### <span data-ttu-id="ecbd8-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ecbd8-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ecbd8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecbd8-129">OUTPUTS</span></span>

### <span data-ttu-id="ecbd8-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecbd8-130">System.Boolean</span></span>

## <span data-ttu-id="ecbd8-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecbd8-131">NOTES</span></span>

## <span data-ttu-id="ecbd8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecbd8-132">RELATED LINKS</span></span>

[<span data-ttu-id="ecbd8-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="ecbd8-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="ecbd8-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ecbd8-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


