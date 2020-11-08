---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184442"
---
# <span data-ttu-id="d4d48-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4d48-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="d4d48-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4d48-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d48-103">A naplózott kategóriák és időgabonák beolvasása</span><span class="sxs-lookup"><span data-stu-id="d4d48-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="d4d48-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4d48-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4d48-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4d48-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d48-106">A **Get-AzDiagnosticSetting** parancsmag az erőforráshoz naplózott kategóriákat és időpontokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d4d48-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="d4d48-107">Az időgabona a metrika összesítési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="d4d48-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="d4d48-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d4d48-108">EXAMPLES</span></span>

### <span data-ttu-id="d4d48-109">Példa 1: a naplózási kategóriák és az időgabona állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="d4d48-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="d4d48-110">Ez a parancs beolvassa az Azure Key Vault-ba bejelentkezve álló kategóriákat és időpontokat a/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="d4d48-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="d4d48-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4d48-111">PARAMETERS</span></span>

### <span data-ttu-id="d4d48-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d48-112">-DefaultProfile</span></span>
<span data-ttu-id="d4d48-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4d48-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4d48-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4d48-114">-Name</span></span>
<span data-ttu-id="d4d48-115">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="d4d48-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="d4d48-116">Ha nem adja meg a "szolgáltatás" alapértelmezett hívását a korábbi API-ban.</span><span class="sxs-lookup"><span data-stu-id="d4d48-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="d4d48-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4d48-117">-ResourceId</span></span>
<span data-ttu-id="d4d48-118">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4d48-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="d4d48-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d48-119">CommonParameters</span></span>
<span data-ttu-id="d4d48-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4d48-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d48-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d4d48-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d48-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4d48-122">INPUTS</span></span>

### <span data-ttu-id="d4d48-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d4d48-123">System.String</span></span>

## <span data-ttu-id="d4d48-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4d48-124">OUTPUTS</span></span>

### <span data-ttu-id="d4d48-125">Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="d4d48-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d4d48-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4d48-126">NOTES</span></span>

## <span data-ttu-id="d4d48-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4d48-127">RELATED LINKS</span></span>

<span data-ttu-id="d4d48-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="d4d48-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
