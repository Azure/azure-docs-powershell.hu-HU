---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c8f05c7ca9ddeb5868d62633600d63f5d7f01be0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492901"
---
# <span data-ttu-id="170d3-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="170d3-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="170d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="170d3-102">SYNOPSIS</span></span>
<span data-ttu-id="170d3-103">Engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="170d3-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="170d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="170d3-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="170d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="170d3-105">DESCRIPTION</span></span>
<span data-ttu-id="170d3-106">A **set-AzureRmApiManagementTenantAccess** parancsmag engedélyezi vagy letiltja a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="170d3-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="170d3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="170d3-107">EXAMPLES</span></span>

### <span data-ttu-id="170d3-108">1. példa: a bérlői hozzáférés engedélyezése</span><span class="sxs-lookup"><span data-stu-id="170d3-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="170d3-109">Ez a parancs engedélyezi a bérlői hozzáférést a megadott környezetben.</span><span class="sxs-lookup"><span data-stu-id="170d3-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="170d3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="170d3-110">PARAMETERS</span></span>

### <span data-ttu-id="170d3-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="170d3-111">-Context</span></span>
<span data-ttu-id="170d3-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="170d3-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="170d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170d3-113">-DefaultProfile</span></span>
<span data-ttu-id="170d3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="170d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="170d3-115">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="170d3-115">-Enabled</span></span>
<span data-ttu-id="170d3-116">Megadja, hogy ez a parancsmag engedélyezi vagy tiltja-e a bérlői hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="170d3-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="170d3-117">Adja meg a letiltáshoz vagy az $False engedélyezéséhez $True értékét.</span><span class="sxs-lookup"><span data-stu-id="170d3-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="170d3-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="170d3-118">-PassThru</span></span>
<span data-ttu-id="170d3-119">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementAccessInformation** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="170d3-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="170d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170d3-120">CommonParameters</span></span>
<span data-ttu-id="170d3-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="170d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170d3-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170d3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170d3-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="170d3-123">INPUTS</span></span>

### <span data-ttu-id="170d3-124">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="170d3-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="170d3-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="170d3-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="170d3-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="170d3-126">OUTPUTS</span></span>

### <span data-ttu-id="170d3-127">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="170d3-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="170d3-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="170d3-128">NOTES</span></span>

## <span data-ttu-id="170d3-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="170d3-129">RELATED LINKS</span></span>

[<span data-ttu-id="170d3-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="170d3-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)


