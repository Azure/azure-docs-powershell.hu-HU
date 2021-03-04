---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 1685b9607108fa0b7795fb0ed2c69eb94735fc5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932097"
---
# <span data-ttu-id="830f4-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="830f4-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="830f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="830f4-102">SYNOPSIS</span></span>
<span data-ttu-id="830f4-103">Engedélyezi vagy letiltja a bérlő hozzáférését.</span><span class="sxs-lookup"><span data-stu-id="830f4-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="830f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="830f4-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="830f4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="830f4-105">DESCRIPTION</span></span>
<span data-ttu-id="830f4-106">A **Set-AzApiManagementTenantAccess** parancsmag engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="830f4-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="830f4-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="830f4-107">EXAMPLES</span></span>

### <span data-ttu-id="830f4-108">1. példa: Bérlői hozzáférés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="830f4-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="830f4-109">Ez a parancs lehetővé teszi a bérlő hozzáférését a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="830f4-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="830f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="830f4-110">PARAMETERS</span></span>

### <span data-ttu-id="830f4-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="830f4-111">-Context</span></span>
<span data-ttu-id="830f4-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="830f4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="830f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830f4-113">-DefaultProfile</span></span>
<span data-ttu-id="830f4-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="830f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="830f4-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="830f4-115">-Enabled</span></span>
<span data-ttu-id="830f4-116">Azt adja meg, hogy ez a parancsmag engedélyezi vagy letiltja-e a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="830f4-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="830f4-117">Adja meg a letiltani $True vagy letiltani $False értéket.</span><span class="sxs-lookup"><span data-stu-id="830f4-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830f4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="830f4-118">-PassThru</span></span>
<span data-ttu-id="830f4-119">Azt jelzi, hogy ez a parancsmag a **psApiManagementAccessInformation** értéket adja vissza, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="830f4-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="830f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830f4-120">CommonParameters</span></span>
<span data-ttu-id="830f4-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830f4-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="830f4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830f4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="830f4-123">INPUTS</span></span>

### <span data-ttu-id="830f4-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="830f4-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="830f4-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="830f4-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="830f4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="830f4-126">OUTPUTS</span></span>

### <span data-ttu-id="830f4-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="830f4-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="830f4-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="830f4-128">NOTES</span></span>

## <span data-ttu-id="830f4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="830f4-129">RELATED LINKS</span></span>

[<span data-ttu-id="830f4-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="830f4-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)


