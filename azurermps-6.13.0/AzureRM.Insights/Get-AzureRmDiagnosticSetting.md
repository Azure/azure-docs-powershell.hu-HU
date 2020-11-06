---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2b70fd58bd0b51e03079b1c24665b67ac3ad3a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496104"
---
# <span data-ttu-id="f7ff9-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="f7ff9-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="f7ff9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ff9-103">A naplózott kategóriák és időgabonák beolvasása</span><span class="sxs-lookup"><span data-stu-id="f7ff9-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7ff9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7ff9-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ff9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ff9-106">A **Get-AzureRmDiagnosticSetting** parancsmag az erőforráshoz naplózott kategóriákat és időpontokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f7ff9-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="f7ff9-107">Az időgabona a metrika összesítési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="f7ff9-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="f7ff9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f7ff9-108">EXAMPLES</span></span>

### <span data-ttu-id="f7ff9-109">Példa 1: a naplózási kategóriák és az időgabona állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f7ff9-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="f7ff9-110">Ez a parancs beolvassa az Azure Key Vault-ba bejelentkezve álló kategóriákat és időpontokat a/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="f7ff9-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="f7ff9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7ff9-111">PARAMETERS</span></span>

### <span data-ttu-id="f7ff9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ff9-112">-DefaultProfile</span></span>
<span data-ttu-id="f7ff9-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f7ff9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7ff9-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7ff9-114">-Name</span></span>
<span data-ttu-id="f7ff9-115">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="f7ff9-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="f7ff9-116">Ha nem adja meg a "szolgáltatás" alapértelmezett hívását a korábbi API-ban.</span><span class="sxs-lookup"><span data-stu-id="f7ff9-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="f7ff9-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7ff9-117">-ResourceId</span></span>
<span data-ttu-id="f7ff9-118">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7ff9-118">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ff9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ff9-119">CommonParameters</span></span>
<span data-ttu-id="f7ff9-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7ff9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ff9-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ff9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ff9-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7ff9-122">INPUTS</span></span>

### <span data-ttu-id="f7ff9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f7ff9-123">System.String</span></span>

## <span data-ttu-id="f7ff9-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7ff9-124">OUTPUTS</span></span>

### <span data-ttu-id="f7ff9-125">Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="f7ff9-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="f7ff9-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7ff9-126">NOTES</span></span>

## <span data-ttu-id="f7ff9-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7ff9-127">RELATED LINKS</span></span>

<span data-ttu-id="f7ff9-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="f7ff9-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
