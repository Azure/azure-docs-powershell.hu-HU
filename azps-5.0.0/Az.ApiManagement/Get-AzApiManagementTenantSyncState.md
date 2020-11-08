---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186467"
---
# <span data-ttu-id="172e9-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="172e9-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="172e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="172e9-102">SYNOPSIS</span></span>
<span data-ttu-id="172e9-103">A konfigurációs adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="172e9-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="172e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="172e9-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="172e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="172e9-105">DESCRIPTION</span></span>
<span data-ttu-id="172e9-106">A **Get-AzApiManagementTenantSyncState** parancsmag a beállítási adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="172e9-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="172e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="172e9-107">EXAMPLES</span></span>

### <span data-ttu-id="172e9-108">Példa 1: a legutóbbi szinkronizálás állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="172e9-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="172e9-109">Ez a parancs a konfigurációs adatbázis és a git repository közötti legutóbbi szinkronizálás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="172e9-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="172e9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="172e9-110">PARAMETERS</span></span>

### <span data-ttu-id="172e9-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="172e9-111">-Context</span></span>
<span data-ttu-id="172e9-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="172e9-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="172e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="172e9-113">-DefaultProfile</span></span>
<span data-ttu-id="172e9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="172e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="172e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="172e9-115">CommonParameters</span></span>
<span data-ttu-id="172e9-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="172e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="172e9-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="172e9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="172e9-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="172e9-118">INPUTS</span></span>

### <span data-ttu-id="172e9-119">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="172e9-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="172e9-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="172e9-120">OUTPUTS</span></span>

### <span data-ttu-id="172e9-121">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="172e9-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="172e9-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="172e9-122">NOTES</span></span>

## <span data-ttu-id="172e9-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="172e9-123">RELATED LINKS</span></span>
