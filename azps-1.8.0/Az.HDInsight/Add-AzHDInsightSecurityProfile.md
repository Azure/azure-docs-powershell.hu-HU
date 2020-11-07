---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 712e3a6f90e37a38584ba27ab1ef07da019dc06a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836086"
---
# <span data-ttu-id="2df01-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2df01-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="2df01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2df01-102">SYNOPSIS</span></span>
<span data-ttu-id="2df01-103">Felvesz egy biztonsági profileto a fürtkonfigurációs objektumba.</span><span class="sxs-lookup"><span data-stu-id="2df01-103">Adds a security profileto a cluster configuration object.</span></span>

## <span data-ttu-id="2df01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2df01-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2df01-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2df01-105">DESCRIPTION</span></span>
<span data-ttu-id="2df01-106">A biztonsági profil segítségével biztonságos fürtöt hozhat létre a kerberizing.</span><span class="sxs-lookup"><span data-stu-id="2df01-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="2df01-107">A biztonsági profil a fürt Active Directory-tartományhoz való csatlakozásának konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2df01-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="2df01-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2df01-108">EXAMPLES</span></span>

### <span data-ttu-id="2df01-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2df01-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2df01-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="2df01-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="2df01-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2df01-111">PARAMETERS</span></span>

### <span data-ttu-id="2df01-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="2df01-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="2df01-113">A Ambari és a Rangerben elérhető Active Directory-csoportok megkülönböztető nevei</span><span class="sxs-lookup"><span data-stu-id="2df01-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df01-114">-Config</span><span class="sxs-lookup"><span data-stu-id="2df01-114">-Config</span></span>
<span data-ttu-id="2df01-115">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="2df01-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="2df01-116">Ezt az objektumot az New-AzHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2df01-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2df01-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df01-117">-DefaultProfile</span></span>
<span data-ttu-id="2df01-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2df01-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2df01-119">-Tartomány</span><span class="sxs-lookup"><span data-stu-id="2df01-119">-Domain</span></span>
<span data-ttu-id="2df01-120">A fürt Active Directory-tartománya</span><span class="sxs-lookup"><span data-stu-id="2df01-120">Active Directory domain for the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df01-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="2df01-121">-DomainUserCredential</span></span>
<span data-ttu-id="2df01-122">A tartomány felhasználói fiókjának hitelesítő adatai, megfelelő engedélyekkel a fürt létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="2df01-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="2df01-123">A Felhasználónév user@domain formátuma</span><span class="sxs-lookup"><span data-stu-id="2df01-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df01-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="2df01-124">-LdapsUrls</span></span>
<span data-ttu-id="2df01-125">Az Active Directory egy vagy több LDAP-kiszolgálójának URL-címei</span><span class="sxs-lookup"><span data-stu-id="2df01-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df01-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="2df01-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="2df01-127">A szervezeti egység megkülönböztetett neve az Active Directoryban, ahol a felhasználói és a számítógépfiókok létrejönnek</span><span class="sxs-lookup"><span data-stu-id="2df01-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df01-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2df01-128">-Confirm</span></span>
<span data-ttu-id="2df01-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2df01-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df01-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df01-130">-WhatIf</span></span>
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

### <span data-ttu-id="2df01-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df01-131">CommonParameters</span></span>
<span data-ttu-id="2df01-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2df01-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df01-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df01-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df01-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2df01-134">INPUTS</span></span>

### <span data-ttu-id="2df01-135">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2df01-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="2df01-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2df01-136">OUTPUTS</span></span>

### <span data-ttu-id="2df01-137">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2df01-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="2df01-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2df01-138">NOTES</span></span>

## <span data-ttu-id="2df01-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2df01-139">RELATED LINKS</span></span>
