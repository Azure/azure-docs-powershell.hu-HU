---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightSecurityProfile.md
ms.openlocfilehash: 7ea9f9d9bb07cae6db62c51b9d496f7117eee700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502724"
---
# <span data-ttu-id="f1623-101">Add-AzureRmHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f1623-101">Add-AzureRmHDInsightSecurityProfile</span></span>

## <span data-ttu-id="f1623-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1623-102">SYNOPSIS</span></span>
<span data-ttu-id="f1623-103">Felvesz egy biztonsági profileto a fürtkonfigurációs objektumba.</span><span class="sxs-lookup"><span data-stu-id="f1623-103">Adds a security profileto a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1623-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1623-104">SYNTAX</span></span>

```
Add-AzureRmHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1623-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1623-105">DESCRIPTION</span></span>
<span data-ttu-id="f1623-106">A biztonsági profil segítségével biztonságos fürtöt hozhat létre a kerberizing.</span><span class="sxs-lookup"><span data-stu-id="f1623-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="f1623-107">A biztonsági profil a fürt Active Directory-tartományhoz való csatlakozásának konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f1623-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="f1623-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f1623-108">EXAMPLES</span></span>

### <span data-ttu-id="f1623-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1623-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f1623-110">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="f1623-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="f1623-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1623-111">PARAMETERS</span></span>

### <span data-ttu-id="f1623-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="f1623-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="f1623-113">A Ambari és a Rangerben elérhető Active Directory-csoportok megkülönböztető nevei</span><span class="sxs-lookup"><span data-stu-id="f1623-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="f1623-114">-Config</span><span class="sxs-lookup"><span data-stu-id="f1623-114">-Config</span></span>
<span data-ttu-id="f1623-115">Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="f1623-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="f1623-116">Ezt az objektumot az New-AzureRmHDInsightClusterConfig parancsmag hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f1623-116">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="f1623-117">-Tartomány</span><span class="sxs-lookup"><span data-stu-id="f1623-117">-Domain</span></span>
<span data-ttu-id="f1623-118">A fürt Active Directory-tartománya</span><span class="sxs-lookup"><span data-stu-id="f1623-118">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="f1623-119">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="f1623-119">-DomainUserCredential</span></span>
<span data-ttu-id="f1623-120">A tartomány felhasználói fiókjának hitelesítő adatai, megfelelő engedélyekkel a fürt létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="f1623-120">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="f1623-121">A Felhasználónév user@domain formátuma</span><span class="sxs-lookup"><span data-stu-id="f1623-121">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="f1623-122">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="f1623-122">-LdapsUrls</span></span>
<span data-ttu-id="f1623-123">Az Active Directory egy vagy több LDAP-kiszolgálójának URL-címei</span><span class="sxs-lookup"><span data-stu-id="f1623-123">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="f1623-124">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="f1623-124">-OrganizationalUnitDN</span></span>
<span data-ttu-id="f1623-125">A szervezeti egység megkülönböztetett neve az Active Directoryban, ahol a felhasználói és a számítógépfiókok létrejönnek</span><span class="sxs-lookup"><span data-stu-id="f1623-125">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="f1623-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1623-126">-Confirm</span></span>
<span data-ttu-id="f1623-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1623-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1623-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1623-128">-WhatIf</span></span>
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

### <span data-ttu-id="f1623-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1623-129">-DefaultProfile</span></span>
<span data-ttu-id="f1623-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1623-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1623-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1623-131">CommonParameters</span></span>
<span data-ttu-id="f1623-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1623-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1623-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1623-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1623-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1623-134">INPUTS</span></span>

### <span data-ttu-id="f1623-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="f1623-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="f1623-136">A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f1623-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="f1623-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1623-137">OUTPUTS</span></span>

### <span data-ttu-id="f1623-138">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="f1623-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="f1623-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1623-139">NOTES</span></span>

## <span data-ttu-id="f1623-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1623-140">RELATED LINKS</span></span>

