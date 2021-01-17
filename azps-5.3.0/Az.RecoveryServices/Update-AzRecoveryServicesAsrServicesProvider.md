---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378305"
---
# <span data-ttu-id="f46c7-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f46c7-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="f46c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f46c7-103">Frissíti (frissítse a kiszolgálót) az Azure webhely-helyreállítási szolgáltatótól kapott adatokat.</span><span class="sxs-lookup"><span data-stu-id="f46c7-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="f46c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f46c7-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f46c7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f46c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f46c7-106">Az **Update-AzRecoveryServicesAsrServicesProvider** parancsmag frissíti az Azure webhely-helyreállítási szolgáltatótól kapott információkat.</span><span class="sxs-lookup"><span data-stu-id="f46c7-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="f46c7-107">Ezzel a parancsmagkal elindíthatja a helyreállítási szolgáltatótól kapott információk frissítését.</span><span class="sxs-lookup"><span data-stu-id="f46c7-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="f46c7-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f46c7-108">EXAMPLES</span></span>

### <span data-ttu-id="f46c7-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="f46c7-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="f46c7-110">Elindítja a megadott ASR-szolgáltatótól származó adatok frissítését, és visszaadja a művelet nyomon követéséhez használt ASR-feladatot.</span><span class="sxs-lookup"><span data-stu-id="f46c7-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f46c7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f46c7-111">PARAMETERS</span></span>

### <span data-ttu-id="f46c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46c7-112">-DefaultProfile</span></span>
<span data-ttu-id="f46c7-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f46c7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f46c7-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46c7-114">-InputObject</span></span>
<span data-ttu-id="f46c7-115">Megadja azt az ASR-szolgáltató-objektumot, amely azonosítja azt a kiszolgálót, amelynek az adatait frissíteni (frissíteni kell.)</span><span class="sxs-lookup"><span data-stu-id="f46c7-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f46c7-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f46c7-116">-Confirm</span></span>
<span data-ttu-id="f46c7-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f46c7-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46c7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46c7-118">-WhatIf</span></span>
<span data-ttu-id="f46c7-119">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f46c7-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f46c7-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f46c7-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46c7-121">CommonParameters</span></span>
<span data-ttu-id="f46c7-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46c7-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f46c7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46c7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f46c7-124">INPUTS</span></span>

### <span data-ttu-id="f46c7-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f46c7-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="f46c7-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46c7-126">OUTPUTS</span></span>

### <span data-ttu-id="f46c7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRService</span><span class="sxs-lookup"><span data-stu-id="f46c7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f46c7-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f46c7-128">NOTES</span></span>

## <span data-ttu-id="f46c7-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f46c7-129">RELATED LINKS</span></span>

[<span data-ttu-id="f46c7-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f46c7-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="f46c7-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="f46c7-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
