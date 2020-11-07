---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 41923067729b50a77f8660a7f626ac464619aa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835089"
---
# <span data-ttu-id="cbc40-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cbc40-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="cbc40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbc40-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc40-103">A naplózott kategóriák és időgabonák beolvasása</span><span class="sxs-lookup"><span data-stu-id="cbc40-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="cbc40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbc40-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbc40-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbc40-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc40-106">A **Get-AzDiagnosticSetting** parancsmag az erőforráshoz naplózott kategóriákat és időpontokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cbc40-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="cbc40-107">Az időgabona a metrika összesítési intervalluma.</span><span class="sxs-lookup"><span data-stu-id="cbc40-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="cbc40-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cbc40-108">EXAMPLES</span></span>

### <span data-ttu-id="cbc40-109">Példa 1: a naplózási kategóriák és az időgabona állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="cbc40-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="cbc40-110">Ez a parancs beolvassa az Azure Key Vault-ba bejelentkezve álló kategóriákat és időpontokat a/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault. *ResourceId* .</span><span class="sxs-lookup"><span data-stu-id="cbc40-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="cbc40-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbc40-111">PARAMETERS</span></span>

### <span data-ttu-id="cbc40-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc40-112">-DefaultProfile</span></span>
<span data-ttu-id="cbc40-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cbc40-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbc40-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbc40-114">-Name</span></span>
<span data-ttu-id="cbc40-115">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="cbc40-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="cbc40-116">Ha nem adja meg a "szolgáltatás" alapértelmezett hívását a korábbi API-ban.</span><span class="sxs-lookup"><span data-stu-id="cbc40-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="cbc40-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbc40-117">-ResourceId</span></span>
<span data-ttu-id="cbc40-118">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cbc40-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="cbc40-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc40-119">CommonParameters</span></span>
<span data-ttu-id="cbc40-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbc40-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc40-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc40-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc40-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbc40-122">INPUTS</span></span>

### <span data-ttu-id="cbc40-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cbc40-123">System.String</span></span>

## <span data-ttu-id="cbc40-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbc40-124">OUTPUTS</span></span>

### <span data-ttu-id="cbc40-125">Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="cbc40-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="cbc40-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbc40-126">NOTES</span></span>

## <span data-ttu-id="cbc40-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbc40-127">RELATED LINKS</span></span>

<span data-ttu-id="cbc40-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="cbc40-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
