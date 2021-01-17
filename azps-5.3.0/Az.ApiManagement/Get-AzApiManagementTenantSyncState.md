---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478889"
---
# <span data-ttu-id="a4c53-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="a4c53-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="a4c53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c53-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c53-103">A konfigurációs adatbázis és a Git-tárház közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4c53-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a4c53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a4c53-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4c53-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a4c53-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c53-106">A **Get-AzApiManagementTenantSyncState** parancsmag megkapja a konfigurációs adatbázis és a Git-tárház közötti legújabb szinkronizálás állapotát.</span><span class="sxs-lookup"><span data-stu-id="a4c53-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a4c53-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a4c53-107">EXAMPLES</span></span>

### <span data-ttu-id="a4c53-108">1. példa: A legutóbbi szinkronizálás állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="a4c53-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="a4c53-109">Ez a parancs a konfigurációs adatbázis és a Git-tárház közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a4c53-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="a4c53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4c53-110">PARAMETERS</span></span>

### <span data-ttu-id="a4c53-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a4c53-111">-Context</span></span>
<span data-ttu-id="a4c53-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="a4c53-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a4c53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c53-113">-DefaultProfile</span></span>
<span data-ttu-id="a4c53-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4c53-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c53-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c53-115">CommonParameters</span></span>
<span data-ttu-id="a4c53-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c53-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c53-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4c53-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c53-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4c53-118">INPUTS</span></span>

### <span data-ttu-id="a4c53-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a4c53-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="a4c53-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4c53-120">OUTPUTS</span></span>

### <span data-ttu-id="a4c53-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="a4c53-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="a4c53-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a4c53-122">NOTES</span></span>

## <span data-ttu-id="a4c53-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4c53-123">RELATED LINKS</span></span>
