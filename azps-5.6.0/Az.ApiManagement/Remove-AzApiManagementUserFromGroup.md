---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 03073dc6116595c93b2c25d30b38c5467482903c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010950"
---
# <span data-ttu-id="7441a-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="7441a-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="7441a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7441a-102">SYNOPSIS</span></span>
<span data-ttu-id="7441a-103">Eltávolít egy felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="7441a-103">Removes a user from a group.</span></span>

## <span data-ttu-id="7441a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7441a-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7441a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7441a-105">DESCRIPTION</span></span>
<span data-ttu-id="7441a-106">A **Remove-AzApiManagementUserFromGroup** parancsmag eltávolít egy felhasználót egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="7441a-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="7441a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7441a-107">EXAMPLES</span></span>

### <span data-ttu-id="7441a-108">1. példa: Felhasználó eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="7441a-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="7441a-109">Ez a parancs eltávolítja a felhasználót egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="7441a-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="7441a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7441a-110">PARAMETERS</span></span>

### <span data-ttu-id="7441a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7441a-111">-Context</span></span>
<span data-ttu-id="7441a-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="7441a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="7441a-113">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="7441a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7441a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7441a-114">-DefaultProfile</span></span>
<span data-ttu-id="7441a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7441a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7441a-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="7441a-116">-GroupId</span></span>
<span data-ttu-id="7441a-117">Annak a csoportnak az azonosítója, amelyből a felhasználót el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="7441a-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="7441a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7441a-118">-PassThru</span></span>
<span data-ttu-id="7441a-119">Azt jelzi, hogy ez a parancsmag $True, ha sikeres, vagy egy $False értéket.</span><span class="sxs-lookup"><span data-stu-id="7441a-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="7441a-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="7441a-120">-UserId</span></span>
<span data-ttu-id="7441a-121">A csoportból eltávolítható felhasználó azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7441a-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="7441a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7441a-122">CommonParameters</span></span>
<span data-ttu-id="7441a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7441a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7441a-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7441a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7441a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7441a-125">INPUTS</span></span>

### <span data-ttu-id="7441a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7441a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7441a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7441a-127">System.String</span></span>

### <span data-ttu-id="7441a-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7441a-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7441a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7441a-129">OUTPUTS</span></span>

### <span data-ttu-id="7441a-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7441a-130">System.Boolean</span></span>

## <span data-ttu-id="7441a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7441a-131">NOTES</span></span>

## <span data-ttu-id="7441a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7441a-132">RELATED LINKS</span></span>

[<span data-ttu-id="7441a-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="7441a-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="7441a-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7441a-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


