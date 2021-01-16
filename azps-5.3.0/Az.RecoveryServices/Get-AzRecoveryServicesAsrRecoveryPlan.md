---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476746"
---
# <span data-ttu-id="39c40-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c40-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="39c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c40-102">SYNOPSIS</span></span>
<span data-ttu-id="39c40-103">Helyreállítási tervet vagy a helyreállítási szolgáltatások tárolóban tárolt összes helyreállítási tervet lekérte</span><span class="sxs-lookup"><span data-stu-id="39c40-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="39c40-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39c40-104">SYNTAX</span></span>

### <span data-ttu-id="39c40-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39c40-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39c40-106">ByName</span><span class="sxs-lookup"><span data-stu-id="39c40-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39c40-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="39c40-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39c40-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39c40-108">DESCRIPTION</span></span>
<span data-ttu-id="39c40-109">A **Get-AzRecoveryServicesAsrRecoveryPlan** parancsmag lekérte a megadott helyreállítási terv vagy az összes helyreállítási csomag részleteit a Helyreállítási szolgáltatások tárolóban.</span><span class="sxs-lookup"><span data-stu-id="39c40-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="39c40-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39c40-110">EXAMPLES</span></span>

### <span data-ttu-id="39c40-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="39c40-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="39c40-112">A megadott nevű helyreállítási tervet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39c40-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="39c40-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c40-113">PARAMETERS</span></span>

### <span data-ttu-id="39c40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c40-114">-DefaultProfile</span></span>
<span data-ttu-id="39c40-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39c40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="39c40-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="39c40-116">-FriendlyName</span></span>
<span data-ttu-id="39c40-117">A lekért helyreállítási terv rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39c40-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c40-118">-Name</span><span class="sxs-lookup"><span data-stu-id="39c40-118">-Name</span></span>
<span data-ttu-id="39c40-119">A lekért helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39c40-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c40-120">-Path</span><span class="sxs-lookup"><span data-stu-id="39c40-120">-Path</span></span>
<span data-ttu-id="39c40-121">Megadja azt a fájl elérési útját, amelybe ez a parancsmag menti a helyreállítási terv json-definícióját.</span><span class="sxs-lookup"><span data-stu-id="39c40-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="39c40-122">A json-definíció szerkeszthető a helyreállítási terv módosításához és a helyreállítási terv frissítéséhez a Update-AzRecoveryServicesASRRecoveryPlan parancsmagon keresztül</span><span class="sxs-lookup"><span data-stu-id="39c40-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c40-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c40-123">CommonParameters</span></span>
<span data-ttu-id="39c40-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c40-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c40-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39c40-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c40-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39c40-126">INPUTS</span></span>

### <span data-ttu-id="39c40-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="39c40-127">None</span></span>

## <span data-ttu-id="39c40-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39c40-128">OUTPUTS</span></span>

### <span data-ttu-id="39c40-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c40-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="39c40-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39c40-130">NOTES</span></span>

## <span data-ttu-id="39c40-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39c40-131">RELATED LINKS</span></span>

[<span data-ttu-id="39c40-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c40-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="39c40-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c40-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="39c40-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39c40-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
