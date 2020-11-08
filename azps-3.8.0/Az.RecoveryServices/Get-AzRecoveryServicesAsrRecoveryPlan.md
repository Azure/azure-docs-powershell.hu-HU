---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010610"
---
# <span data-ttu-id="489e1-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="489e1-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="489e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="489e1-102">SYNOPSIS</span></span>
<span data-ttu-id="489e1-103">Helyreállítási terv vagy az összes helyreállítási csomag beszerzése a helyreállítási szolgáltatások pincéjében</span><span class="sxs-lookup"><span data-stu-id="489e1-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="489e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="489e1-104">SYNTAX</span></span>

### <span data-ttu-id="489e1-105">Alapértelmezett (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="489e1-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="489e1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="489e1-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="489e1-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="489e1-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="489e1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="489e1-108">DESCRIPTION</span></span>
<span data-ttu-id="489e1-109">A **Get-AzRecoveryServicesAsrRecoveryPlan** parancsmag a helyreállítási szolgáltatások pincéjében megadott helyreállítási terv vagy minden helyreállítási csomag részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="489e1-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="489e1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="489e1-110">EXAMPLES</span></span>

### <span data-ttu-id="489e1-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="489e1-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="489e1-112">A megadott nevű helyreállítási csomagot kapja.</span><span class="sxs-lookup"><span data-stu-id="489e1-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="489e1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="489e1-113">PARAMETERS</span></span>

### <span data-ttu-id="489e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="489e1-114">-DefaultProfile</span></span>
<span data-ttu-id="489e1-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="489e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="489e1-116">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="489e1-116">-FriendlyName</span></span>
<span data-ttu-id="489e1-117">A beolvasott helyreállítási terv rövid nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="489e1-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="489e1-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="489e1-118">-Name</span></span>
<span data-ttu-id="489e1-119">A beolvasott helyreállítási terv nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="489e1-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="489e1-120">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="489e1-120">-Path</span></span>
<span data-ttu-id="489e1-121">Annak a fájlnak az elérési útvonalát adja meg, amelybe a parancsmag a helyreállítási terv JSON-definícióját menti.</span><span class="sxs-lookup"><span data-stu-id="489e1-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="489e1-122">A JSON-definíció szerkeszthető a helyreállítási terv módosításához és a helyreállítási terv Update-AzRecoveryServicesASRRecoveryPlan parancsmagon keresztüli frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="489e1-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="489e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489e1-123">CommonParameters</span></span>
<span data-ttu-id="489e1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="489e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489e1-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="489e1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489e1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="489e1-126">INPUTS</span></span>

### <span data-ttu-id="489e1-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="489e1-127">None</span></span>

## <span data-ttu-id="489e1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="489e1-128">OUTPUTS</span></span>

### <span data-ttu-id="489e1-129">Microsoft. Azure. Command. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="489e1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="489e1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="489e1-130">NOTES</span></span>

## <span data-ttu-id="489e1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="489e1-131">RELATED LINKS</span></span>

[<span data-ttu-id="489e1-132">Új – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="489e1-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="489e1-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="489e1-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="489e1-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="489e1-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
